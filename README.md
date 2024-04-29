def get_password_length():
    while True:
        try:
            length = int(input("Enter the desired length of the password: "))
            if length > 0:
                return length
            else:
                print("Invalid input. Please enter a positive integer.")
        except ValueError:
            print("Invalid input. Please enter a positive integer.")
            import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password
    def display_password(password):
    print(f"Generated password: {password}")
    def main():
    length = get_password_length()
    password = generate_password(length)
    display_password(password)

if _name_ == '_main_':
    main()
