# PRODIGY_CS_01
def caesar_cipher(text, shift, mode):
    result = ""
    
    # Adjust shift for decryption
    if mode == "decrypt":
        shift = -shift

    for char in text:
        if char.isalpha():
            start = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - start + shift) % 26 + start)
        else:
            result += char
    return result


def main():
    print("Caesar Cipher Program")
    mode = input("Choose mode (encrypt/decrypt): ").strip().lower()

    # Validate mode input
    if mode not in ["encrypt", "decrypt"]
        print("Invalid mode. Please choose 'encrypt' or 'decrypt'.")
        return

    text = input("Enter the message: ")
    shift = int(input("Enter shift value (integer): "))

    result = caesar_cipher(text, shift, mode)
    print(f"\nResult: {result}")


if __name__ == "__main__":
    main()
