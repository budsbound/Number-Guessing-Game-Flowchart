# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateNumber[Generate Random Number]
    GenerateNumber --> UserInput[Get User Input]
    UserInput --> CheckInput{Is Input Valid?}
    
    CheckInput -- Yes --> Compare{Is Guess Correct?}
    CheckInput -- No --> InvalidInput[Display Error Message]
    InvalidInput --> UserInput
    
    Compare -- Correct --> CorrectGuess([Correct!])
    Compare -- TooHigh --> HighGuess([Too High!])
    Compare -- TooLow --> LowGuess([Too Low!])
    
    HighGuess --> UserInput
    LowGuess --> UserInput
    CorrectGuess --> End([End])
