# Dragonfruit-AI_assignment
### Question 1. Efficient Data Structure to store the images
**Microscopic Image**:
- As the parasite body is known to be a blob like structure of arbitrary shape which wil be a continuous region of black pixels, it will be most efficient to use ***Run-Length-Encoding (RLE)*** for the microscopic image.
- RLE encodes the image as the starting posiion of the pixel and its run-length. However, to ***optimise*** more in terms of space, we only encode black pixels as encoding both white and black pixels would take unnecessary space.
- Each tuple in the RLE list takes 8 bytes (4 for the starting position and 4 for the run length).
- Assuming the blob to be of circular shape, and occupying an area of 25% in the image which means that the radius of that circle will be approx. 15,000 pixels. Therefore, the number of elements in the RLE list would be approx. 30,000 (1 element per row). The total memory occupied will approx. be 240,000 bytes ≈ 234.4 KB.
- In the worst case, is the parasite occupies each complete image area, there will be 100,000 elements in the RLE data. Hence, in this case, the occupied memory will be 781.25 KB. This proves the storage efficiency of the chosen data structure.

**Dye Sensor Image**:
- In this case, the dye will be sparsely located in the image. Therefore, it will be most efficient to store only the coordinates which are lit. Hence, we use a sparse representation to store the images. For that, we chose the list data structure in python that will only store the coordinates from the image that are lit.
- In the worst case, the dye will acquire all the area of the parasite body. Therefore, would require the memory equal to 4*parasite_body_area which can be approx. 37.26 GB (if the parasite body acquires all the area in the image).
- However, this case is very unrealistic. Therefore, assuming that the dye acquires 30% of the total parsite body area and the parasite body area is 50% of the total image area, the required memory for the dye sensor image would be approx. 1 GB.
