def calculate_discount(price, discount_percent):
    """Calculate final price after applying discount if >= 20%."""
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        # No discount applied
        return price


# Get input from the user
try:
    price = float(input("Enter the original price: "))
    discount_percent = float(input("Enter the discount percentage: "))

    # Calculate the final price
    final_price = calculate_discount(price, discount_percent)

    # Display the result
    if discount_percent >= 20:
        print(f"The final price after {discount_percent}% discount is: ${final_price:.2f}")
    else:
        print(f"No discount applied. The price remains: ${final_price:.2f}")

except ValueError:
    print("Please enter valid numeric values for price and discount.")
# function
