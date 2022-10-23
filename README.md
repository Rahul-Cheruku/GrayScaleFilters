Let’s understand some of the few important filters:
For Arithmetic mean,
Average (or mean) filtering is a method of 'smoothing' images by reducing the amount of intensity variation between neighbouring pixels. The average filter works by moving through the image pixel by pixel, replacing each value with the average value of neighbouring pixels, including itself.
The Arithmetic Mean (AM) or called average is the ratio of the sum of all observations to the total number of observations.
Here the observations are the intensity of all pixels in in given 3x3, 7x7 etc masking. 
We take these pixel intensity and replace the center pixel intensity with final mean value.
	  	Arithmetic mean = ∑_(-k)^k▒  ∑_(-j)^j▒I_(r+k,c+j)  
(Sum of all pixel intensity in masking)
	Where k,j = floor(scale) 
	Eg. For scale = 3,
	k = {-1, 0, 1} 		j = {-1, 0, 1} 
	Arithmetic mean filter is commonly used for noise reduction.

For Geometric mean,
Geometric Mean=  ( ∏_(-k)^k▒  ∏_(-j)^j▒I_(r+k,c+j) )  ^(1/(k.j))
The geometric mean filter is most widely used to filter out Gaussian noise.

For median filter,
	
	Step 1: Arrange all intensities of mask in ascending or descending order.
	Step2:  Let n = total no of intensities in mask
		
 Median= {█((n+1)/2 th term @((n/2 th  term+(n/2+1)th term)/2) )    █(For n=odd@ @ @ )¦(For n=even)  ┤ 

It is very effective at removing impulse noise, the “pepper and salt” noise, in an image. The principle of the median filter is to replace the gray level of each pixel by the median of the gray levels in a neighborhood of the pixels, instead of using the average operation.

For Max filter,
New intensity=Max of |I_1,〖 I〗_2,I_3…..|
MaxFilter is a nonlinear filter commonly used to locally smooth data and diminish pepper-like noise, where the amount of smoothing is dependent on the value of r. The function applied to each range-r neighborhood is Max.

For Min filter,
New intensity=Min of |I_1,〖 I〗_2,I_3…..|
MinFilter is a nonlinear filter commonly used to locally smooth data and diminish salt-like noise, where the amount of smoothing is dependent on the value of r. The function applied to each range-r neighborhood is Min. 

For Midpoint filter,
The midpoint filter is typically used to filter images containing short tailed noise such as Gaussian and uniform type noises. The midpoint filter is defined as : where the coordinate (x+i, y+j ) is defined over the image A and the coordinate (i, j) is defined over the N x N size square mask.
New intensity=(Max of |I_1,〖 I〗_2,I_3…..|+ Min of |I_1,〖 I〗_2,I_3…..|)/2
