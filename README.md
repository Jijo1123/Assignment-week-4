try:
    # Prompt the user for the source filename
    source_filename = input("Enter the filename to read: ")

    # Open the source file to read
    with open(source_filename, "r") as source_file:
        content = source_file.read()

    print("File content successfully read.\n")

    # Modify the content (e.g., make it uppercase)
    modified_content = content.upper()

    # Prompt the user for the destination filename
    destination_filename = input("Enter the filename to save the modified content: ")

    # Write the modified content to the destination file
    with open(destination_filename, "w") as destination_file:
        destination_file.write(modified_content)

    print(f"File has been modified and written to '{destination_filename}'.")

except FileNotFoundError:
    print("Error: The source file does not exist.")
except PermissionError:
    print("Error: You do not have permission to read or write to the specified file.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
    
