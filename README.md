import turtle

# Set up the screen
screen = turtle.Screen()
screen.bgcolor("white")

# Create a turtle object
flower = turtle.Turtle()
flower.shape("turtle")
flower.speed(10)

# Function to draw a flower petal
def draw_petal():
    flower.circle(100, 60)  # Draw an arc (half-circle)
    flower.left(120)        # Turn the turtle
    flower.circle(100, 60)  # Draw another arc

# Function to draw the full flower
def draw_flower():
    for _ in range(6):      # Draw 6 petals
        draw_petal()
        flower.left(60)     # Turn the turtle to position for the next petal

# Drawing the flower
flower.color("red")
draw_flower()

# Hide the turtle and display the window
flower.hideturtle()
screen.mainloop()
