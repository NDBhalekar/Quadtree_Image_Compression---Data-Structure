# Quadtree_Image_Compression---Data-Structure
# Image Compression Using Quad Trees

## 📌 Overview

Quadtrees are used for image compression by recursively dividing an image into four subregions. Each region stores the average RGB color of its pixels, reducing image complexity and approximating the original image.

## ⚙️ Requirements

- Linux environment
- C/C++ compiler and `make`
- Input images in **PPM format**
- Input images must have the same dimensions when comparing them

## 🚀 How to Run

### Step 1: Compile the project

```bash
make
```

### Step 2: Compress an image

```bash
./compress -c <compression_level> <input_image> <output_image>
```

**Example:**

```bash
./compress -c 5 input.ppm output.ppm
```

Replace `5` with your desired compression level and the filenames with your actual image paths.

## 🖼️ Input and Output

- The program accepts images in **PPM format only**.
- The output image remains in PPM format.
- The input and output images have the same dimensions.
- To observe the file-size difference, compare the original and compressed images after converting them to a suitable image format or by checking their file sizes.

## 🔄 Converting Image Formats on Linux

You can use ImageMagick's `convert` command to convert PPM images to other formats and vice versa.

**PPM to PNG:**

```bash
convert input.ppm output.png
```

**PNG to PPM:**

```bash
convert input.png output.ppm
```

Install ImageMagick if it is not already available:

```bash
sudo apt install imagemagick
```

## 🧠 How It Works

1. Divide the image into four subregions.
2. Calculate the average RGB color for each region.
3. Recursively divide regions according to the compression criteria.
4. Represent regions using their average colors to approximate the original image.

## 📝 Note

The output PPM image may have the same dimensions as the input image. Image dimensions and file size are different properties, so equal dimensions do not necessarily mean equal file sizes.
