# Finance-calculator
import math

class FinanceCalculator:
    def __init__(self):
        self.balance = 0
        self.tax_rate = 0.2
        self.home_price = 0
        self.building_cost = 0

    def add_balance(self, amount):
        self.balance += amount

    def calculate_tax(self, amount):
        return amount * self.tax_rate

    def calculate_home_price(self, down_payment_percent):
        down_payment = self.home_price * (down_payment_percent / 100)
        mortgage_amount = self.home_price - down_payment
        return mortgage_amount

    def calculate_building_cost(self, square_feet, cost_per_square_foot):
        self.building_cost = square_feet * cost_per_square_foot
        return self.building_cost

    def solve_complex_equation(self, equation):
        try:
            result = eval(equation)
            return result
        except Exception as e:
            return f"Error: {e}"

# Example usage
calculator = FinanceCalculator()

calculator.add_balance(10000)
print(f"Current Balance: ${calculator.balance}")

tax_amount = calculator.calculate_tax(5000)
print(f"Tax Amount: ${tax_amount}")

calculator.home_price = 200000
mortgage_amount = calculator.calculate_home_price(down_payment_percent=10)
print(f"Mortgage Amount: ${mortgage_amount}")

building_cost = calculator.calculate_building_cost(square_feet=1500, cost_per_square_foot=100)
print(f"Building Cost: ${building_cost}")

equation_result = calculator.solve_complex_equation("2 * (3 + 4) / 5")
print(f"Complex Equation Result: {equation_result}")
