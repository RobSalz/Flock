---
title: Document Center
---

# Deep Learning Training Machine Tech Spec

### Tim Dettmers Guide
A great guide on the hardware requirements for deep-network training. The post looks at possible bottle necks and what really matters for training.
http://timdettmers.com/2015/03/09/deep-learning-hardware-guide/

### Facebook Rig 12x4 Gb VRAM
This is Facebooks Development Rig adapted from the NVIDIA suggestion:
- https://www.facebook.com/notes/chris-lengerich/build-your-own-nvidia-devbox/10152999419281541/
- http://pcpartpicker.com/p/PhVv99

I substituted components that I couldn't find in South Africa for the ones marked *

    -Motherboard: GA-X99-UD4                                                (R  4,945.00)
    -Processor: Core i7-5930K                                               (R 11,481.00)
    -GPU: 4 x ASUS Titan X                                                  (R 22,294.00 x 4)
    -Case: Carbide Series® Air 540 High Airflow ATX Cube Case               (R  2,482.00)
    -Power Supply: EVGA 1600 P2                                             (R  7,654.00)
    -Memory: Viper Extreme 32GB (4 x 8GB)  *Corsair Vengence                (R  5,266.00)
    -Disks: Samsung XP941 M.2 (512GB)      *Evo 850                         (R  3,199.00)
    -CPU Cooler: Corsair H60                                                (R  1,462.00)
     Total with 4 TITAN X                                                    R 125,665.00
     Total with 3 TITAN X                                                    R 103,371.00
     Total with 2 TITAN X                                                    R  81,077.00
     Total with 1 TITAN X                                                    R  58,783.00

Facebook did their homework here, I agree with all their choices. Great Value for money!
### Smaller Version 12x2 Gb VRAM

    -Motherboard: GA-X99-UD4                                                (R  4,945.00)
    -Processor: Core i7-5930K                                               (R 11,481.00)
    -GPU: 2 x ASUS Titan X                                                  (R 22,294.00 x 2)
    -Case: Carbide Series® Air 540 High Airflow ATX Cube Case               (R  2,482.00)
    -Power Supply: EVGA 1200 P2                                             (R  4,736.00)
    -Memory: Corsair Vengence 32GB (4 x 8GB)                                (R  3,799.00)
    -Disks: Samsung Evo 850 (512GB)                                         (R  3,199.00)
    -CPU Cooler: Corsair H60                                                (R  1,462.00)
     Total with 2 TITAN X                                                    R 76,692.00 - 12 Gb VRAM
     Total with 1 TITAN X                                                    R 54,398.00 - 24 Gb VRAM

Scaled down the power supply as 2 Titans are more than enough. Training will just take longer.

### Starter Dev 6-12 Gb VRAM

    -Motherboard: GA-X99-UD4                                                (R  4,945.00)
    -Processor: Core i7-5930K                                               (R 11,481.00)
    -GPU: EVGA GTX 980Ti Superclocked                                       (R 14,699.00)
    -Case: Use current case                                                 (R      0.00)
    -Power Supply: EVGA 1200 P2                                             (R  4,736.00)
    -Memory: Corsair Vengence 16GB (2 x 8GB)                                (R  2,030.00)
    -Disks: Samsung Evo 850 (512GB)                                         (R  3,199.00)
    -CPU Cooler: Corsair H60                                                (R  1,462.00)
     Total with 1 GTX 980Ti                                                  R 42,552.00 - 6 Gb VRAM
     Total with 2 GTX 980Ti                                                  R 57,251.00 - added on later (12Gb)
     Total with 1 TITAN X                                                    R 50,147.00 - 12 Gb VRAM

Using my case and starting out with one GTX 980Ti will get us going for now. The machine is still super fast. A second card could be added later. Lower RAM required for this build; more can be added if a third card is required (or two Titans).

### Super Starter Dev 4-8 Gb VRAM

    -Motherboard: Asus Z170 Pro Gaming                                      (R  3,772.00)
    -Processor: Intel Core i5-6500                                          (R  3,799.00)
    -GPU: Gigabyte GTX 960                                                  (R  5,199.00)
    -Case: Use current case                                                 (R      0.00)
    -Power Supply: EVGA 1000 G2                                             (R  3,494.00)
    -Memory: Viper Extreme 8GB (2 x 4GB)  *Corsair Vengence                 (R  1,158.00)
    -Disks: Samsung XP941 M.2 (256GB)      *Evo 850                         (R  1,729.00)
    -CPU Cooler: Corsair H60                                                (R  1,462.00)
     Total with 1 GTX 960                                                    R 20,613.00 - 4 Gb VRAM
     Total with 2 GTX 960                                                    R 25,812.00 - 8 Gb VRAM
     Total with 1 TITAN X                                                    R 37,708.00 - 12 Gb VRAM

This is a value for money rig. All the components are slower and from the previous generation. However, for stricly convolutional network training, the CPU, Motherboard and RAM should not bottleneck the GPU's. Therefore, a Titan X could still be used effectivley. I have scaled down the power supply, RAM and nard drive. The power supply and RAM will have to be upgraded if more cards are installed.

 #### Notes
 1. All prices found at www.wootware.co.za for comparison
 2. Certain components may be found for appox 8% cheaper at Rectron
 3. Certain components for the Super Starter rig may be found second hand at www.carbonite.co.za
