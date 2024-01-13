
# Project3-part2

In this section, we want to investigate the following stochastic process and draw average and autocorrelation graphs and compare them with theoretically obtained functions.


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/83cd72fa-7dc9-4135-9a75-c36777078f00)


First, we obtain the mean and the autocorrelation function of the random process and then determine the type of the process.


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/d8770350-4c2d-43b7-b38f-2a3069317081)


Considering that the mean is zero, it means that it is independent of time, and the autocorrelation function is independent of time, that is, it is not a function of t, but only a function of τ, so the type of process is WSS.

In this section, we draw the random process and average it with respect to theta.

![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/f5c663f9-6bfc-4474-9a7d-4cb871a561eb)


According to the obtained autocorrelation function, we draw the autocorrelation diagram of the process in three dimensions.


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/4d8c2bf8-ea6b-4fbc-b85f-94bcf0c3f572)


We draw the average and correlation functions obtained in the theoretical mode (the average was obtained as zero).


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/e7189c0f-fbf9-4e2b-8afa-4d041e31147a)

![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/46aa88d9-15c3-41c4-9481-231a22a8ecaf)


The mean function obtained from the theoretical relations is slightly different from the mean function drawn in MATLAB. The mean function drawn in MATLAB is in cosine form, but due to the small range, it can be ignored. And in the figures of autocorrelation functions, we also find that considering that the graph drawn with the help of MATLAB is three-dimensional, in order to compare the two, we have to look at them in two-dimensional form, in this case, we realize that the graphs of autocorrelation drawn are similar is.

To obtain the stationary process, we average with respect to t using the implementation of the autocorrelation function.


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/94cfbd9c-6ace-42ba-8b78-44320005e658)

# Project3-part3
Introduction to digital communication - quantization
In this project, we learn about converting analog signals to digital and sending and detecting digital signals. First, an analog signal is converted into a discrete signal in the transmitter, and using quantization levels, the amplitude values of the transmitted pulses are determined in digital communications. Then this process is repeated in reverse in the receiver and interpolation is used to convert discrete to continuous signal.

We generate and plot the given signal with N = 50,000 samples



![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/368db57a-943a-4144-9610-0ee6d08b13da)




In this part, we sample the analog signal with a sampling frequency of 500 Hz and generate a discrete-time signal.



![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/48b92e4b-2394-49ce-8d24-6eca823f11b5)




For quantization, use the uniform quantization type. For this purpose, we consider 32 quantization levels. Then plot the sampled values to the nearest level. The image of the quantized signal is as follows.


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/d1753f45-d2ef-4bc8-8b86-358f4fd8c4ac)



In this section, for each quantized point, according to digital modulations, we send a triangular pulse in the transmitter. In fact, to digitize the quantized signal, we send each sampled point as a triangular pulse with a certain amplitude. .
1- The energy of the discrete time signal obtained by sampling the triangular signal with a frequency of 1000 Hz is equal to: 333.3340
2- We store the signal value of each level with the corresponding digit in a two-dimensional array. We use this array to recover the signal. We use gray code coding; Each of the symbols is coded in this way and the corresponding pulse is found and finally, by placing these pulses next to each other, we draw the shape of the digital signal resulting from this modulation.


![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/38d6710b-29d3-4a61-ae72-d9c241895a35)


In the receiver, the received signal will be accompanied by noise, for this we consider the channel noise as Gaussian noise, and according to the definition, it is a normal random process, and we get the noise according to the SNR in the receiver.
Finally, we draw the input signal of the receiver (after adding noise).



![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/523c791c-e7d8-4ce6-ace0-eb15cd3eb67b)



At this stage, we go through the process of recovering the analog signal from the digital, we must know that each of the pulses assigned to each digit is a multiple of the base pulse and each of the symbols is sent in 1 second.
1- We multiply the basic pulse by the pulse string received in the receiver, for every second, and by calculating their mutual energy and considering the energy of the basic pulse, we find the amplitude of each of these pulses and in this way, Using the bit string sent for each symbol, we specify the digit of the quantization level.
Then we convert the values on the quantization levels
2- Using the obtained two-dimensional array, we convert each digit to the actual value of the signal at the quantization level and draw the shape of the resulting signal.



​![image](https://github.com/MatinNekoonam82/Project3-part3/assets/156523741/4b92be7d-c74a-4b88-afda-e9a118d3b757)


it is obvious that decoded message is as same as the quantized signal 






