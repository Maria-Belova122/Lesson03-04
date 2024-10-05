# ЗАДАНИЕ ПО ТЕМЕ "Произвольное число параметров"

def single_root_words(root_word, *other_words):
    same_words = []
    for i in range(len(other_words)):
        word = other_words[i].lower()
        root_word_1 = root_word.lower()
        if word.find(root_word_1) != -1 or root_word_1.find(word) != -1:
            same_words.append(other_words[i])
    return same_words


result1 = single_root_words('rich', 'Richiest', 'orichalcum', 'cheers', 'RICHIES')
result2 = single_root_words('Disablement', 'ABLE', 'Mable', 'Disable', 'Bagel')
result3 = single_root_words('лоток', 'околоток', 'ЛОТО', 'потолок', 'ток')
result4 = single_root_words('a123', 'A12', 'b23', 'CBA12345', '321a')
print(result1)
print(result2)
print(result3)
print(result4)
