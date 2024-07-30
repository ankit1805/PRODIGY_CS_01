import tkinter as tk
from tkinter import messagebox

def caesar_encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            ascii_offset = 65 if char.isupper() else 97
            result += chr((ord(char) - ascii_offset + shift) % 26 + ascii_offset)
        else:
            result += char
    return result

def caesar_decrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            ascii_offset = 65 if char.isupper() else 97
            result += chr((ord(char) - ascii_offset - shift) % 26 + ascii_offset)
        else:
            result += char
    return result

def encrypt():
    text = input_text.get("1.0", "end-1c")
    shift = int(shift_entry.get())
    encrypted_text = caesar_encrypt(text, shift)
    output_text.delete("1.0", "end")
    output_text.insert("1.0", encrypted_text)

def decrypt():
    text = input_text.get("1.0", "end-1c")
    shift = int(shift_entry.get())
    decrypted_text = caesar_decrypt(text, shift)
    output_text.delete("1.0", "end")
    output_text.insert("1.0", decrypted_text)

def clear():
    input_text.delete("1.0", "end")
    shift_entry.delete(0, "end")
    output_text.delete("1.0", "end")

root = tk.Tk()
root.title("Caesar Cipher")

input_label = tk.Label(root, text="Input Text:")
input_label.pack()

input_text = tk.Text(root, height=10, width=40)
input_text.pack()

shift_label = tk.Label(root, text="Shift Value:")
shift_label.pack()

shift_entry = tk.Entry(root, width=40)
shift_entry.pack()

encrypt_button = tk.Button(root, text="Encrypt", command=encrypt)
encrypt_button.pack()

decrypt_button = tk.Button(root, text="Decrypt", command=decrypt)
decrypt_button.pack()

clear_button = tk.Button(root, text="Clear", command=clear)
clear_button.pack()

output_label = tk.Label(root, text="Output Text:")
output_label.pack()

output_text = tk.Text(root, height=10, width=40)
output_text.pack()

root.mainloop()
