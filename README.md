# ASSESMENT--2
import time

MIN_BRIGHTNESS = 0
MAX_BRIGHTNESS = 10
STEP_SIZE = 1

brightness = 5


print("LED Brightness Control")
print("Press '+' to increase brightness")
print("Press '-' to decrease brightness")
print("Press 'q' to quit")

while True:

    print(f"Brightness: {'|' * brightness} ({brightness})")

    
    command = input("Enter command (+/-/q): ").strip()

    if command == '+':
        if brightness < MAX_BRIGHTNESS:
            brightness += STEP_SIZE
        else:
            print("Brightness is at maximum limit!")
    elif command == '-':
        if brightness > MIN_BRIGHTNESS:
            brightness -= STEP_SIZE
        else:
            print("Brightness is at minimum limit!")
    elif command == 'q':
        print("Exiting LED Brightness Control.")
        break
    else:
        print("Invalid command! Use '+' to increase, '-' to decrease, or 'q' to quit.")

    time.sleep(0.5)  
