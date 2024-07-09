# password-creation
mport random
import string

def generate_password(length):
    lower = string.ascii_lowercase
    upper = string.ascii_uppercase
    digits = string.digits
    special = string.punctuation
    all_characters = lower + upper + digits + special
    password = ''.join(random.choice(all_characters) for _ in range(length))
    return password
def main():
    print("Password Generator")
    while True:
        try:
            length = int(input("Enter the desired length of the password: "))
            if length <= 0:
                print("Please enter a positive number.")
                continue
            break
        except ValueError:
            print("Please enter a valid number.")
    password = generate_password(length)
    print(f"Generated password: {password}")

if __name__ == "__main__":
    main()
