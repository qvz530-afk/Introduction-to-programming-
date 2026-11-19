START

    INPUT loan amount
    INPUT penalty rate
    CONVERT penalty rate to decimal
    INPUT repayment period in months

    SET balance = loan amount
    SET month = 1

    WHILE balance > 0 DO

        DISPLAY month

        INPUT repayment amount
        SUBTRACT repayment amount from balance

        IF balance <= 0 THEN
            SET balance = 0
            DISPLAY "Loan fully repaid!"
            BREAK
        END IF

        IF month >= repayment period THEN
            CALCULATE penalty = balance * penalty rate
            ADD penalty to balance
            DISPLAY penalty added
        END IF

        DISPLAY remaining balance

        INCREASE month by 1

    END WHILE

    DISPLAY final balance

END
