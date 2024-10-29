def trigonometry():
    print("Select trigonometric function:")
    print("1. Sin")
    print("2. Cos")
    print("3. Tan")
    print("4. Inverse Sin")
    print("5. Inverse Cos")
    print("6. Inverse Tan")

    choice = input("Enter your choice (1-6): ")
    try:
        if choice in {'1', '2', '3'}:
            angle = float(input("Enter the angle in degrees: "))
            angle_rad = math.radians(angle)  # Convert degrees to radians
            if choice == '1':
                result = math.sin(angle_rad)
            elif choice == '2':
                result = math.cos(angle_rad)
            elif choice == '3':
                result = math.tan(angle_rad)
        elif choice in {'4', '5', '6'}:
            value = float(input("Enter the value (must be in the range -1 to 1 for inverse functions): "))
            if choice == '4':
                if value < -1 or value > 1:
                    print("Error: Input must be between -1 and 1.")
                    return
                result = math.asin(value)
            elif choice == '5':
                if value < -1 or value > 1:
                    print("Error: Input must be between -1 and 1.")
                    return
                result = math.acos(value)
            elif choice == '6':
                result = math.atan(value)
        else:
            print("Invalid choice.")
            return
        
        print(f"The result is: {result}")
    
    except ValueError:
        print("Error: Invalid input. Please enter numeric values.")