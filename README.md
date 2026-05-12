# My_learning

# to download old version repository from artifact repository use the below commands


* gcloud --version   (# to check the version of the gcloud)
* gcloud auth login (# to help you login with the correct credentials)
* gcloud storage cp gs://run-sources-birlaopusai-asia-south1/services/automation-bwz/1777018212.718000.zip .  (# from gs............. your path of the cloud function along with the version that you want to download,   "." location on which you want to copy this)
* unzip 1777018212.718000.zip  (# the repository file is usually zip to unzip is required) (# if this didn't work then use the below tar one)
* tar -xf 1777018212.718000.zip  
* ls
* dir
* cd base.py (# base.py is one of your file from the unzipped file)

# 
* Client
 *  ↓
* Client Portal
  * ↓
* GCS Bucket - Uncleaned
*   ↓
* automation_bwz
*   ├── File Cleaning
*   ├── Validation
 *  ├── Transformation 
 *  	└── Notifications / Error Tracking
  * 	└── GCS Bucket - Cleaned
 *  			↓
* BigQuery Tables
*   ├── Till GSR Flow
*   │     ├── Calculations
 *  │     └── Email + Excel to Client
  │* 
  * └── New Revised GSR Flow
    *     ├── Rate Creation from Working File
      *   ├── ZSD CN / Scheme Calculations
    *     ├── Email Summary to Client
    *     ├── automation_bwz_load
    *     ├── Append to YTD BigQuery Table
   *      ├── Power BI Dashboard
   *      └── Archive Handling
     *            ├── ZSD / Taxable / Scheme Mapping = Merge-based
     *            └── Other files = Latest-file based
