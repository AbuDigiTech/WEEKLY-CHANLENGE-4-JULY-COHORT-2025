This is the first line of text.
This is the second line of text.
This is the third line of text.
This is the fourth line of text.
This is the fifth line of text.

def process_file(input_file, output_file):
    try:
        # Read the contents of the input file
        with open(input_file, 'r') as file:
            content = file.read()

        # Count the number of words in the file
        word_count = len(content.split())

        # Convert all text to uppercase
        processed_content = content.upper()

        # Write the processed text and the word count to the output file
        with open(output_file, 'w') as file:
            file.write(processed_content)
            file.write(f"\n\nWord Count: {word_count}")

        # Print a success message
        print(f"File processed successfully. Output written to {output_file}")

    except FileNotFoundError:
        print(f"File {input_file} not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

def main():
    input_file = 'input.txt'
    output_file = 'output.txt'
    process_file(input_file, output_file)

if __name__ == "__main__":
    main()
