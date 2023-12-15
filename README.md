# Loop-5
# Problem 5: Extended Price with Discounts

# Initialize variables
total_discounts = 0.0

# Prompt user to continue
user_input = input("Do you want to continue? (Yes/No): ")

# Use a while loop based on user input
while user_input.lower() == "yes":
    # Prompt user for item data
    quantity = int(input("Enter quantity: "))
    price = float(input("Enter price of an item: "))
    
    # Calculate extended price
    extended_price = quantity * price
    
    # Apply discount based on extended price
    if extended_price > 10000.00:
        discount_percent = 0.25
    else:
        discount_percent = 0.10
    
    # Calculate discount amount and total
    discount_amount = extended_price * discount_percent
    total = extended_price - discount_amount
    
    # Display results
    print(f"Extended Price: ${extended_price:.2f}")
    print(f"Discount Amount: ${discount_amount:.2f}")
    print(f"Total: ${total:.2f}")
    
    # Update total discounts
    total_discounts += discount_amount
    
    # Prompt user to continue
    user_input = input("Do you want to continue? (Yes/No): ")

# Display total discounts
print(f"\nTotal Discounts: ${total_discounts:.2f}")
