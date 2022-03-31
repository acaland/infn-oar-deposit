# INFN OAR Bulk Deposit

This command line tool allows to deposit a set of records to the INFN Open Access Repository (or any Zenodo based one) from a list of metadata stored in YAML file.
(to be continued)


## Requirements

Python3 (and `pip`) should be installed on your machine


## 📋 Installation

1. Clone this repository into a folder of your local machine:
   
   ```
   git clone https://github.com/acaland/infn-oar-deposit.git
   ```

   Alternatively you can download the source from https://github.com/acaland/infn-oar-deposit/archive/refs/heads/master.zip

2. Using the Terminal app (macOS) or PowerShell (Windows) navigate to the folder where you cloned/unzipped the source code:

   ```
   cd <path_to_infn-oar-deposit>
   ```

   Alternatively you can use Visual Studio Code and its integrated terminal. In this case you need just to open the folder with the source code. VS Code defaults the terminal to the root of your opened workspace.

3. (Optional) Create a Python virtual environment and activate it. With `venv` for example:
   
   ```
   python -m venv .oar
   
   # Activate the virtual environment (macOS/Linux)
   $ source .oar/bin/activate

   # Activate the virtual environment (Windows)
   PS C:> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   PS C:\> .oar\Scripts\activate.ps1

   ```

4. Install the needed dependencies with:

   ```
   pip install -r requirements.txt
   ```

  5. If you haven't already created a _Personal Access Token_ to access INFN OAR API, go to https://www.openaccessrepository.it/account/settings/applications/ and create a **New Token**. Copy the new token and save it in a safe place as you cannot retrieve it again. 
   
  6. Create a `.env` file in the same folder as `oar-deposit.py` with the line:
     ```bash
     OAR_TOKEN=<your_personal_token_from_OAR_here>
     ```
     Alternatively, you can set an environment variable into your system. For example, :

     ```
     # on macOS/*nix environment
     $ export OAR_TOKEN=<your_personal_token_from_OAR_here>

     # on Windows
     PS C:\> $env:OAR_TOKEN="<your_personal_token_from_OAR_here>"
     ```



  ## 🚀 Usage
  
  1. (Optional) Load the virtual environment where you set up infn-oar-deposit:
     ```
     # macOS/*nix
     $ source <path_to_infn-oar-deposit>/.oar/bin/activate
     
     # Windows
     PS C:\> .<path_to_infn-oar-deposit>\Scripts\activate.ps1
     ```
  
  2. (Optional) Set your OAR_TOKEN env variable (if you don't use the `.env` file)
  
  3. Start the bulk deposit script with:   
     ```
     python oar-deposit.py <path_of_the_yml_file>     <record_number_to_deposit>
     ```
     
     where `<record_number_to_deposit>` is the **i-th** records listed in the .YAML file




