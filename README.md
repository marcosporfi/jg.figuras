import turtle

# Função para desenhar um quadrado maior
def desenhar_quadrado(cor):
    turtle.fillcolor(cor)
    turtle.begin_fill()
    for _ in range(4):
        turtle.forward(200)  # Aumentado
        turtle.left(90)
    turtle.end_fill()

# Função para desenhar um triângulo maior
def desenhar_triangulo(cor):
    turtle.fillcolor(cor)
    turtle.begin_fill()
    for _ in range(3):
        turtle.forward(200)  # Aumentado
        turtle.left(120)
    turtle.end_fill()

# Função para desenhar um círculo maior
def desenhar_circulo(cor):
    turtle.fillcolor(cor)
    turtle.begin_fill()
    turtle.circle(100)  # Raio aumentado
    turtle.end_fill()

# Função principal
def main():
    print("Selecione uma forma:")
    print("1 - Quadrado")
    print("2 - Triângulo")
    print("3 - Círculo")
    forma = input("Digite o número da forma desejada: ")

    print("\nEscolha uma cor: red, blue, green, yellow")
    cor = input("Digite o nome da cor (em inglês): ").lower()

    turtle.speed(3)
    turtle.penup()
    turtle.goto(0, 0)
    turtle.pendown()

    if forma == '1':
        desenhar_quadrado(cor)
    elif forma == '2':
        desenhar_triangulo(cor)
    elif forma == '3':
        desenhar_circulo(cor)
    else:
        print("Forma inválida!")

    turtle.done()

main()
