import random

num = random.randint(1,100)
detalhe = "um"
tentativa = 0

print("Adivinhe o número, se errar eu lhe direi se baixo, ou Alto em relação ao número real. Comece!")
while True:
    chute = int(input(f"Chute {detalhe} número: "))
    detalhe = "outro"
    tentativa +=1

    if chute != num:
        
        if chute < num:
            print("Está baixo")
        else:
            print("Está alto") 
        continue
    else:
        if tentativa <=4:
            print(f"Parabéns!! O número era {num}, você foi CERTEIRO!, acertou em {tentativa} tentativas.")
        else:
            if tentativa <=8:    
                print(f"Parabéns!! O número era {num}, foi bom mas pode melhorar! Você acertou em {tentativa} tentativas.")
            else: 
                print(f"Parabéns!! O número era {num}, precisa de mais sorte :( ou mais intuição, você acertou em {tentativa} tentativas.")    

    continua = input("Quer continuar? (Y/N): ")    
    match continua.lower():
        case "y":
            continue
        case "n":
            break
