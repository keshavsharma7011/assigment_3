# assigment_3
def most_frequent(string):
    letter_freq = {}
    for letter in string:
        if letter.isalpha():
            letter = letter.lower()
            if letter in letter_freq:
                letter_freq[letter] += 1
            else:
                letter_freq[letter] = 1
    sorted_freq = sorted(letter_freq.items(), key=lambda x: x[1], reverse=True)
    for letter, freq in sorted_freq:
        print(f"{letter}: {freq}")
input_string = "Mississippi"
most_frequent(input_string)
