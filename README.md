# Magic_sphere
# -*- coding: utf-8 -*-
from random import choice
from time import sleep


def answer_to_the_question() -> bool:
    while True:
        answer = input(">>> ").lower()
        if answer == "да":
            return True
        elif answer == "нет":
            return False
        else:
            continue


def main():
    SPHERES_ANSWERS = ["Бесспорно", "Предрешено", "Никаких сомнений", "Определённо да", "Можешь быть уверен в этом",
                       "Мне кажется - да", "Вероятнее всего", "Хорошие перспективы", "Знаки говорят - да", "Да",
                       "Пока неясно, попробуй снова", "Спроси позже", "Лучше не рассказывать",
                       "Сейчас нельзя предсказать",
                       "Сконцентрируйся и спроси опять", "Даже не думай", "Мой ответ - нет", "По моим данным - нет",
                       "Перспективы не очень хорошие", "Весьма сомнительно"]
    print('Привет Мир, я магический шар, и я знаю ответ на любой твой вопрос. \U0001F52E')
    sleep(3)
    name = input("Как тебя зовут? ")
    print(f'Привет {name}')
    while True:
        question = input("Спрашивай, что тебя интересует?\n>>> ")
        if question == '':
            continue
        if not question.endswith("?"):
            print("Это был вопрос? Не совсем понимаю. Давай попробуем ещё раз.")
            continue
        print("Хм...")
        sleep(5)
        print(choice(SPHERES_ANSWERS))
        print(f"У тебя ещё остались какие-то вопросы, {name}?")
        if answer_to_the_question():
            continue
        else:
            print("Возвращайся, если возникнут вопросы!")
            break


if __name__ == "__main__":
    main()
