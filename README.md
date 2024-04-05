# -Robot-Arm-Simulator
This project simulates a simple robot arm using Python's Turtle graphics library
import turtle

# Define robot arm parameters
arm_length1 = 100
arm_length2 = 50

# Initialize Turtle object
pen = turtle.Turtle()
pen.speed(0)  # Set drawing speed to fastest

def move_arm(angle1, angle2):
  """Moves the simulated robot arm to specified angles."""
  pen.setheading(angle1)  # Set base angle
  pen.forward(arm_length1)
  pen.setheading(angle2 + 90)  # Adjust for second arm segment
  pen.forward(arm_length2)
  pen.penup()  # Lift pen to avoid drawing during movement
  pen.setposition(0, 0)  # Return to origin
  pen.pendown()  # Put pen down for next drawing

# Example usage (change angles to see movement)
move_arm(45, 30)
move_arm(-60, 90)

turtle.done()  # Keep window open until closed manually

