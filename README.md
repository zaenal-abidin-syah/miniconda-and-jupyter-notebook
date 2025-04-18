# Installation for miniconda and jupyter
# Starter Guide
 
Step 1: Instalasi Miniconda
### **Windows user**
- Klik link ini untuk download: [Miniconda Windows 64-bit](https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe)

- Install miniconda
    - Ketika ada pilihan `install for`, pilih `Just Me (recommended)`

- Jalankan `Anaconda Prompt`

### **Mac user**
- Download miniconda untuk Python 3.7
    - Klik link ini untuk download: [Miniconda Mac OS X 64-bit](https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.pkg)
    - 
    - Note: skip step ini apabila kamu sudah menggunakan Anaconda sebelumnya. Walau demikian, saya akan jelaskan alasan kenapa kamu sebaiknya menggunakan miniconda nanti di course ini.

- Install miniconda
    - Install tanpa mengubah opsi apapun
    - Tunggu hingga instalasi selesai

- Jalankan terminal

### **Linux user**
- Download miniconda untuk Python 3.7
    - Klik link ini untuk download: [Miniconda Linux 64-bit](https://repo.anaconda.com/miniconda/Miniconda3-py39_23.3.1-0-Linux-x86_64.sh)
    - Note: skip step ini apabila kamu sudah menggunakan Anaconda sebelumnya. Walau demikian, saya akan jelaskan alasan kenapa kamu sebaiknya menggunakan miniconda nanti di course ini.
    
- Install miniconda
    - jalankan terminal or ctrl + T
    - download miniconda
        ```
        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        ```
    - Install miniconda menggunakan command berikut
        ```
        bash Miniconda3-latest-Linux-x86_64.sh
        ```
    - Ketik `yes` untuk agree dengan license nya, kemudian `yes` lagi untuk `prepend miniconda install location to PATH`
    - Tunggu hingga instalasi selesai
    - perintah untuk disable autoactive conda ketika terminal terbuka
      
      ```bash
      conda config --set auto_activate_base false
      ```
      
    
- hanya untuk memastikan, tutup dan buka terminal lagi
### Other
- bisa juga memilih sesuai OS dan versi [repo Miniconda](https://repo.anaconda.com/miniconda/)

## Step 3: Instalasi Jupyter 
- Kita akan install 2 hal di base environment
    
    ```
    conda activate
    OR
    conda activate base
    ```
  - lakukan penginstalan jupyter notebook di environment base saja agar jupyter dapat mengakses atau berpindah ke environment lain perlu menginstall library ipykernel di environment lain agar dikenali jupyter (recommended)
    ```
    conda install -n base -c conda-forge jupyter nb_conda_kernels notebook
    OR
    conda install -n base -c conda-forge jupyter nb_conda_kernels "notebook<7.0" 
    ```
  - install ipykernel di environment lain
    ```
    conda install -n myenv -c conda-forge ipykernel
    ```

## Step 4: Instalasi Environment
- Jalankan command ini untuk menginstall environment `jcopml`
    ```
    conda env create -f your-env.yml
    ```
