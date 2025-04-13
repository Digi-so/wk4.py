
def readfile(me.txt):
    try:
        with open(me.txt, "r") as file:
            content = file.read()
        return content
    except FileNotFoundError:
        print(f"Error: The file '{me.txt}' does not exist.")
        return None
    except Exception as e:
        print(f"Error: An error occurred while reading the file '{me.txt}'. {e}")
        return None

def writefile(filename, content):
    try:
        with open(filename, "w") as file:
            file.write(content)
    except Exception as e:
        print(f"Error: An error occurred while writing to the file '{me.txt}'. {e}")
