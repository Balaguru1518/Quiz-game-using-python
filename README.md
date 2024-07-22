# Quiz-game-using-python
#python quiz game

questions=("Who developed Python Programming Language?:",
           "Which type of Programming does Python support?:",
           "Which of the following is the correct extension of the Python file?:",
           "Which of the following is used to define a block of code in Python language?:",
           "Which keyword is used for function in Python language?:")

options=(("A.Wick van Rossum","B. Rasmus Lerdorf","C.Guido van Rossum","D.Guido van Rossum"),
           ("A.object-oriented programming","B.object-oriented programming","C.functional programming","D.none of thos above"),
           ("A.python","B.pl","C.py","D.p"),
           ("A.Indentation","B.Key","C.Brackets","D. All of the mentioned"),
           ("A. Function","B.def","C.Fun","D.Define"))

answers=("C","D","C","A","B")
gusses=[]
score=0
question_num= 0

for question in questions:
    print("-----------------------------")
    print(question)
    for option in options[question_num]:
        print(option)

    guess = input("Enter (A,B,C,D):").upper()
    gusses.append(guess)
    if guess== answers[question_num]:
        score += 1
        print("CORRECT!")
    else:
        print("INCORRECT!")
        print(f"{answers[question_num]} is the correct answer")
    question_num +=1
 
    

    print("-----------------------------")
    print("          RESULTS            ")
    print("-----------------------------")

    print("answers:", end="")
    for answer in answers:
        print(answer,end=" ")

    print("gusses:", end="")
    for guess in gusses:
        print(guess,end=" ")
    print()

    Score=int(score/len(questions)*100)
    print(f"Your score is: {Score}%")
