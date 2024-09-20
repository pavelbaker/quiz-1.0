import random

def quiz(questions, difficulty, operation):
    score= 0
    difficulty = difficulty.lower()
    
    for j in range(questions):

        if difficulty == "easy":
            a = random.randint(1,10)
            b = random.randint(1,10)
    
        elif difficulty == "medium":
            a = random.randint(1,100)
            b = random.randint(1,100)
        elif difficulty == "hard":
            a = random.randint(1,1000)
            b = random.randint(1,1000)
        else:
            print("This is not a recognised difficuly. Please choose either 'easy', 'medium' or 'hard'.")
            return

        
        if operation == "addition":
            answer = a+b
            operator = "+"
        elif operation == "subtraction":
            answer = a-b
            operator = "-"
        elif operation == "multiplication":
            answer = a*b
            operator = "*"
        elif operation == "division":
            answer = a/b
            operator = "/"
        else:
            print("This is not a recognised operation. Please choose either 'addition', 'subtraction', 'multiplication', or 'division'.")
            return


        while True:
            try:
                user_answer = input(f"What is {a} {operator} {b}? ")

                if operator == "/":
                    user_answer = float(user_answer)
                    if round(user_answer,2) == round(answer, 2):
                        print("You are correct")
                        score +=1
                        break
                    else:
                        print(f"Incorrect, the correct answer was {round(answer, 2)}")
                        break
                else:
                    user_answer = int(user_answer)
                    if user_answer == answer:
                        print("You are correct")
                        score+=1
                        break
                    else:
                        print(f"Incorrect, the correct answer was {answer}")
                        break
            except ValueError:
                print("This is not a number, try again")

    print(f"You got {score} out of {questions}")
