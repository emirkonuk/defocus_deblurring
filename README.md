# Defocus Simulations
In the computer vision community, the usual way of simulating the defocus blur is by convolving the original image with a blur kernel. This kernel is usually chosen to be;
- Gaussian, or
- 2D Bessel kernel (i.e., Airy Disk), or
- A simple disk kernel.

For all of these kernels, the amount of the blur is controlled by the size of the kernel. However, this is not a realistic model of defocus blur. For a more physically meaningful defocus: 
- Zernike Polynomials based defocus aberration, and
- Hanser's method described in [Phase retrieval for high-numerical-aperture optical systems](https://pdfs.semanticscholar.org/7080/134549f2185cd0c41ed6b7d8eddcd60a95cd.pdf),

are implementations can be found in the Notebook. For example, here is a comparison of the Zernike Polynomial based defocus vs. Disk convolution blur:

![Disk Comparison](https://github.com/emirkonuk/defocus_deblurring/blob/master/imgs/zernike_hanser_disk_difference.png)

# Image Restoration 
The implementations of the two fundamental image deblurring algorithms;
- Wiener Filtering, and 
- Richardson Lucy Algorithm

can be found in the Notebook. For example, here is the results of applying a naive inverse filtering vs. Wiener Filtering for both known and unknown Signal-to-Noise ratios in the presence of a small additive noise:

![Wiener Comparison](https://github.com/emirkonuk/defocus_deblurring/blob/master/imgs/wiener_comparison.png)
