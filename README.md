# How I Construct My Data Projects

A comprehensive guide and template for constructing data analysis projects. This repository provides a structured directory layout, guidelines for managing scripts, data, reports, and documentation, as well as integration with various cloud storage and computation services.

## Features
- **Structured Directory Layout**: Organized folders for raw data, processed data, scripts, results, reports, papers, and more.
- **Reproducibility**: Version control for scripts and configuration files to ensure reproducibility of analyses.
- **Cloud Integration**: Scripts and configurations for managing data storage and computation on various cloud services.
- **Documentation**: Guidelines and examples for documenting the analysis process, maintaining logs, and creating reports.
- **Configurable**: Flexible configuration options for specifying data sources, processing methods, and backup strategies.

## Directory Structure

```
project_root/
|
├── README.md                           # Project introduction and usage instructions
├── .git/                               # Git version control folder
├── .gitignore                          # List of files to ignore in git
├── setup/                              # Project setup and initialization scripts
│ ├── init.sh                           # Initialization script to download raw data from cloud services
│ ├── requirements.txt                  # Python dependencies list
│ ├── renv.lock                         # R dependencies lock file
│ ├── aws-s3-backup.sh                  # AWS S3 backup script
│ ├── aws-s3-restore.sh                 # AWS S3 restore script
│ └── aws-ec2-cluster.yaml              # AWS EC2 cluster configuration file
|
├── data/                               # Directory for raw and processed data
│ ├── raw/                              # Raw data (downloaded from cloud services)
│ ├── processed/                        # Processed data (generated locally)
│ ├── config.yaml                       # Data configuration file, specifying data sources and processing methods
│ └── md5sum.txt                        # MD5 checksum file for data integrity verification
├── results/                            # Directory for storing analysis results
|
├── docs/                               # Project documentation
│ ├── notes/                            # Analysis process records
│ │ ├── yyyy-mm-dd.md                   # Records of analysis processes by date
│ │ └── ...
│ ├── TODOs.md                          # List of tasks to be completed
│ ├── changelog.md                      # Record of changes in code and analysis process
│ └── workflow.md                       # Workflow documentation, describing the full analysis process
|
├── notebooks/                          # Jupyter notebooks or other note files
├── scripts/                            # Various script files for analysis and processing
│ ├── script1.sh
│ ├── analysis.py
│ └── process_data.R
├── logs/                               # Directory for storing log files
|
├── references/                         # Directory for reference materials
├── reports/                            # Directory for external reports
│ ├── yyyy-mm-dd_project_report.Rmd     # Rmarkdown format report file
│ ├── yyyy-mm-dd_project_report.html    # Output HTML report
│ ├── yyyy-mm-dd_project_report.pdf     # Output PDF report
│ └── yyyy-mm-dd_attachments/           # Attachments required for the report
├── papers/                             # Directory for paper-related files
│ ├── paper1/                           # Directory for the first paper
│ │ ├── manuscript/                     # Manuscript files
│ │ ├── submission/                     # Submission-related files
│ │ ├── figures/                        # Figures for the paper
│ │ ├── supplementary/                  # Supplementary materials
│ │ └── references/                     # References management
│ ├── paper2/                           # Directory for the second paper
│ └── ...                               # Other papers directories
└── static_site/                        # Directory for generating and publishing static HTML pages
  ├── index.html                        # Static website homepage
  ├── css/                              # CSS files for the static website
  ├── js/                               # JavaScript files for the static website
  └── results/                          # Analysis results pages and attachments
    ├── result1.html                    # First result page
    ├── result2.html                    # Second result page
    └── files/                          # Attachments for the result pages
```

## License

This project is licensed under the [MIT License](LICENSE).
