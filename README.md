# Digital Signal Processing

### heart_rate
This code is used to extract the heart rate from an individual using only a short video clip of the individual. This concept was used in the video calling device that our SDSU team developed for West Health Institute. The code to take a short video and amplify the skin tone variations to reveal the heartbeat was designed by an amazing team at MIT led by Dr. Frédo Durand and Dr. William T. Freeman. [Their project can be found here.](http://people.csail.mit.edu/mrub/vidmag/) 
Our team wanted to use this concept of medical sensing without physical contact, and implemented the MIT code. The code provided by them creates an output video. Further code is needed to extract the heart rate using [Fast Fourier Transform (FFT)](https://en.wikipedia.org/wiki/Fast_Fourier_transform). This code was written to take the center fifth of the frame and average the intensity of red pixels in that region. This information is then processed to find the dominant frequency which can be read as the individual's heart rate. Further improvements can be made by incorporating image stabilization or face tracking, but for our purpose these were not necessary.

### high_res_spectrum_analysis
The objective is to compare the power spectrum estimates produced using several methods, particularly the minimum variance method which is not based on the traditional use of the FFT. The main goal is to compare the vertical variance that is present in the different methods, both qualitatively and quantitatively.

### imperial_march
This project required the noise reduction of a song, The Imperial March from Star Wars. Several types of noise had been added to the audio file, and needed to be removed. The code in imperial_march_fft.m finds the noise. Using this information, four [band stop filters](https://en.wikipedia.org/wiki/Band-stop_filter) were designed and [implemented](http://www.mathworks.com/help/matlab/ref/filter.html) in imperial_march_filter.m. The program produced a noiseless song after several tweaks with the filter parameters. 
