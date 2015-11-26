### OpenCL Histogram Example ###
Approaches where the input image data is a buffer or an image (i.e. an 
image2d_t data type in CL) are implemented.  The input per-pixel data stored in
buffer or image can be a RGBA 8-bit/channel, RGBA half-float/channel or 
RGBA float/channel.

For RGBA 8-bit/channel image data, the histogram is computed for R, G and B
channels.  256-bins for each channel are created.  These 256-bins are stored
in a single histogram buffer.

For RGBA half-float and float image data, the histogram is computed for R, G 
and B channels.  257-bins for each channel are created.  These 257-bins are 
stored in a single histogram buffer.

gpu_histogram.c
gpu_histogram_buffer.cl
gpu_histogram_image.cl
histogram.xcodeproj