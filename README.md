# Merging_multiple_Excel_files
By this code, you can merge multiple excel files into 1 single excel file.

    import os
    import pandas as pd

    input_file_path = "E:/Pedram/Pedram/Folder/"
    output_file_path = "E:/Pedram/Pedram/Folder/New/"
    excel_file_list = os.listdir(input_file_path)

    df = pd.DataFrame()

    for excel_files in excel_file_list:
        if excel_files.endswith(".xlsx"):
            df1 = pd.read_excel(input_file_path + excel_files)
            df = df.append(df1)
            print(excel_files + " - Done")

    df.to_excel(output_file_path+"Final.xlsx")

