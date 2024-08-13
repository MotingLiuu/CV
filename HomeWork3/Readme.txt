There are two ipynb files.
 
My360_COM.ipynb use the sample images.

My360_COM_MyOwnImages.ipynb use the photos taken by myself.

Introduction of My Homework

1. I have completed the Gaussian Pyramid Optical Flow method to stitch multiple images into a single panoramic image.

2. When generating a panoramic image using my own pictures, I only used a portion of the images to create a panorama with an angle of approximately 180 degrees. Since I don't have a camera and tripod, I could only use my handheld phone for shooting, which made it impossible to perfectly capture a 360° view. However, I tried my best to capture a set of photos of the tabletop with my phone, which clearly demonstrates the effect of the program I completed. (Some parameters are different from those used to generated sample panorama).(Use another ipynb file to test)

3. To ensure the stability of the Lucas-Kanade method, I added a small identity matrix when solving the equations to ensure numerical stability.

4. First, I implemented the Lucas-Kanade method to calculate the displacement between images by solving a system of equations. Next, I implemented the iterative Lucas-Kanade method. Then, I generated a Gaussian pyramid by progressively applying Gaussian convolution. In each layer of the Gaussian pyramid generated for the two images, I used the iterative Lucas-Kanade method for alignment. Finally, I created a large blank image and placed each image in its corresponding position in the panorama based on the calculated displacement. The edges of the images were then processed using linear blending, filling the black edges of the images with the corresponding pixels from the previous image. 

5. I have completed the global warp to correct vertical drift, just not print on the screen.