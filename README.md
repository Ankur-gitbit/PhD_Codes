How it Works:
Upload your TSV files - they're saved to uploaded_files_{project_name}

Output directory is automatically set to the same directory as the input files

All generated files (Excel, plots, ZIP) are saved in the same directory

You can still download files from Google Colab as needed

Directory contents are shown at the end for verification


Key Changes Made:
Added Section 4: Set Output Directory: Sets output_dir = upload_dir to save all files in the same directory as input files.

Modified process_all_files function:

Added output_directory parameter

Changed output_filename to output_path using os.path.join(output_directory, output_filename)

Added output directory information to the Overall_Stats sheet

Modified create_individual_plots function:

Added output_directory parameter

Changed all plot file paths to use os.path.join(output_directory, filename)

All plots are now saved directly to the input/output directory

Modified create_results_zip function:

Added output_directory parameter

Search for files in the output directory instead of current directory

Save ZIP file to the output directory

Added show_directory_contents function:

Shows organized view of all files in the directory

Color-coded icons for different file types

Shows file sizes in appropriate units (KB, MB, GB)

Updated function calls to pass the output_dir parameter

Updated final message to show where files were saved
