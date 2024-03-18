# Dragonfruit-AI_assignment
### Question 1
**Microscopic Image**:
- As the parasite body is known to be a blob like structure of arbitrary shape which wil be a continuous region of black pixels, it will be most efficient to use ***Run-Length-Encoding (RLE)*** for the microscopic image.
- RLE encodes the image as the starting posiion of the pixel and its run-length. However, to ***optimise*** more in terms of space, we only encode black pixels as encoding both white and black pixels would take unnecessary space.
- Each tuple in the RLE list takes 8 bytes as the tuple doesn't store the element, it stores the pointer to that element.
- Assuming the blob to be of circular shape, and occupying an area of 25% in the image which means that the radius of that circle will be approx. 15,000 pixels. Therefore, the number of elements in the RLE list would be approx. 30,000 (1 element per row). The total memory occupied will approx. be 240,000 bytes = 234.4 MB.
- In the worst case, is the parasite occupies each complete image area, there will be 100,000 elements in the RLE data. Hence, in this case, the occupied memory will be 781.25 MB. This proves the storage efficiency of the chosen data structure.
