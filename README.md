Download Link: https://assignmentchef.com/product/solved-csci5980-assignment2-image-transformaion
<br>
<h1>1             Camera Calibration</h1>

Figure 1: Lens distortion recification.

Using your cellphone camera, you will estimate intrinsic camera parameters (focal length, principal points, and lens distortion parameter).

<strong>Write-up:</strong>

<ul>

 <li>Derive <strong>K </strong>matrix using your camera specification.</li>

 <li>Calibrate lens distortion using the radial distortion model (single parameter, <em>k</em><sub>1</sub>). Show the original image, undistorted image, and two image examples of wrong <em>k</em><sub>1 </sub>as shown in Figure 1.</li>

</ul>

<h1>2             Projective Line</h1>

Figure 2: (a) You will use your cellphone camera image to compute camera poses with respect to the ground plane and measure the height of your friend given the height of an object. (b) You will paste the UMN logo to the ground plane.

Take a picture of your friend with many 3D objects such as street lamps and chair where two orthogonal directions on the ground plane are visible as shown in Figure 2(a). Apply lens undistortion to make the straight lines straight.

<strong>Write-up:</strong>

<ul>

 <li>Derive and compute two vanishing points and a vanishing line, and visualize them on your image similar to Figure 2(a).</li>

 <li>Compute camera rotation matrix, <strong>R</strong>, and visualize 3D camera axes with respect to the ground plane axes using MATLAB plot3 Give a geometric interpretation of the computed rotation matrix.</li>

 <li>Measure the heights of at least 3D objects given your friend’s height using the cross ratio. Verify the height measurements.</li>

 <li>Project UMN logo onto the ground plane or any planar surface. You are also free to choose different logo or image.</li>

</ul>

<h1>3             Panoramic Image</h1>

<ul>

 <li>Input images</li>

 <li>Geometry</li>

</ul>

φ

<ul>

 <li>Cylindrical coordinate</li>

 <li>Panoramic image</li>

</ul>

Figure 3: Given a collection of input images, you will create a panoramic images by projecting onto a cylindrical surface.

You will create a panoramic image from multiple images (at least 8 images) taken by your cellphone camera using a cylindrical projection as shown in Figure 3(a). The panoramic image will be created in (<em>φ,h</em>) where <em>φ </em>and <em>h </em>are angle and height coordinate of the cylindrical surface, respectively, as shown in Figure 3(c). Note that the radius and height of the cylinder are set to the focal length and height of the image, respectively.

<strong>Write-up:</strong>

T

<ul>

 <li>Express the direction vector <strong>p</strong><em><sub>φ,h</sub></em>using <em>φ </em>and <em>h </em>as shown in</li>

</ul>

Figure 3(c) and 3(b).

<ul>

 <li>Given the first and second images, compute homography, <sup>2</sup><strong>H</strong><sub>1 </sub>using 4 correspondences and relative rotation from first to second, <sup>2</sup><strong>R</strong><sub>1 </sub>where the first image rotation is the identity matrix <strong>I</strong><sub>3</sub>.</li>

</ul>

<em>λ</em><strong>u</strong><sub>2 </sub>= <strong>Hu</strong><sub>1</sub>

<em>µ</em><strong>u</strong>2 = <strong>K</strong>2<strong>R</strong>1<strong>p</strong><em>φ,h                                                                                                                </em>(1)

where <strong>u</strong><sub>1 </sub>&#x2194; <strong>u</strong><sub>2 </sub>is the corresponding points in the first and second image.

<ul>

 <li>For all images, compute the rotation matrix, <em><sup>i</sup></em><strong>R</strong><sub>1</sub>, and visualize the camera Z axis in 3D using MATLAB plot3 <em>Hint</em>: <em><sup>i</sup></em><strong>R</strong><sub>1 </sub>=<em><sup>i </sup></em><strong>R</strong><em><sub>i</sub></em><sub>−1 </sub><em><sup>i</sup></em><sup>−1</sup><strong>R</strong><em><sub>i</sub></em><sub>−2 </sub>···<sup>2</sup><strong>R</strong><sub>1</sub>.</li>

 <li>Create a panoramic image by copying RGB value of original image coordinate (<em>u,v</em>) to the cylindrical coordinate (<em>φ,h</em>) as shown in Figure 3(d). You may blend overlapping pixels by taking average.</li>

</ul>

<strong>Note:</strong>

<ol>

 <li>Rotate your camera about fixed rotation center (no translation). Translation of your camera produces mis-alignment.</li>

 <li>Choose 4 correspondences very carefully.</li>

 <li>Lens distortion may introduce mis-alignment.</li>

 <li>Objects at far distance often work better.</li>

</ol>