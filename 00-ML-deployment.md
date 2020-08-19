# deployment platform
- cloud
buying a huge computation system, people or users get an instance on cloud platforms like AWS, GCP, Microsoft Azure, etc. where it would cost around $150 per month approximately. 
- on-prem
- edge
here has been launched various devices such as Nvidia Jetson TX1, Nano, TX2, Xavier, Raspberry pi, etc with having a programming language binding support like python, c++, etc. by which we can deploy the deep learning model on this devices.These devices have a decent CPU memory, GPU memory with a good resolution camera at an affordable price. 

There are ways to scale down neural networks to fit in our edge devices. An alternate (or complementary) method would be to scale up the performance of the microprocessor.

    1. Raspberry pi 4:

    The Raspberry Pi is a low cost, credit-card sized computer that plugs into a computer monitor or TV, and uses a standard keyboard and mouse. Configuration of this device contains Ram of 4GB, 2 × USB 3.0 ports, 2 x USB 2.0 Ports, 2 × micro HDMI ports supporting up to 4Kp60 video resolution, Micro SD card slot for loading the operating system and data storage.
    Pricing: $61.99 on amazon
    Models that can be run on Raspberry pi 4
For object Detection
— SSD MOBILE NET- 40 FPS
— TinyYOLOV2 -3 FPS
— OpencvDNN- 5 FPS
For Pose estimation
— SSD MOBILE NET with Open Pose- 7 FPS
Face Detection and Recognition
— OpencvDNN — 3 FPS
— Python Face Recognition Library- 2.5 FPS  

2. Nvidia Jetson Nano Series
NVIDIA Jetson Nano enables the development of millions of new small, low-power AI systems. It opens new worlds of embedded IoT applications, including entry-level Network Video Recorders (NVRs), home robots, and intelligent gateways with full analytics capabilities. Nano is a device that is slightly better than raspberry pi 4. The difference is it also provides GPU memory partition which enhances the speed of the model.
Pricing:$99.00 Amazon

3. Azure stack edge with FPGA, or with GPUß
4. Coral devices with Edge TPU