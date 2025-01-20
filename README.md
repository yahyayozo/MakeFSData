# MakeFSData

This Python script converts web files (such as HTML, CSS, JS, images) into a C source structures that will be used by LwIP filesystem for HTTP server. The script processes files by compressing them with gzip and then generating a C file (`fsdata.c`) containing these compressed files as static data arrays.

## Usage

1. **Set the File Path**:
   Update the `FSDATA_FILE_PATH` variable with the desired path for the generated C file, where the data will be embedded.

2. **Directory to Process**:
   The script processes files in the directory `Middlewares/Third_Party/LwIP/src/apps/http/fs`. Ensure that your files are placed within this directory or update the script to use a different directory.

3. **Running the Script**:
   To run the script, simply execute it from the command line using Python:
   ```bash
   python makeFSdata.py
    ```
   
## Example
You can check my [STM32H7_WebServer](https://github.com/yahyayozo/STM32H7_WebServer) as an example on how to run this script to generate the C source files, and use them in a webserver hosted in an MCU.