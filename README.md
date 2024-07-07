def calculate_pay(hours, pay_rate):
    if hours > 40:
        overtime_hours = hours - 40
        overtime_pay = overtime_hours * 1.5 * pay_rate
        regular_pay = 40 * pay_rate

        total_pay = regular_pay + overtime_pay
    else:
        total_pay = hours * rate
    
    return total_pay

# Example usage:
try:
    hours_worked = float(input("Enter hours worked: "))
    hourly_pay_rate = float(input("Enter hourly pay rate: "))

    total_earnings = calculate_pay(hours_worked, hourly_pay_rate)
    print(f"Total earnings: ${total_earnings:.2f}")

except ValueError:
    print("Error: Please enter numerical values for hours worked and hourly pay rate.")
