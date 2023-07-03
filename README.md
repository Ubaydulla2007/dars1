class Talaba:
    def __init__(self, ism, fam, mat, das, kim):
        self.ism = ism
        self.fam = fam
        self.mat = mat
        self.das = das
        self.kim = kim
        self.av = (mat + das + kim) / 3

    def baxo(self):
        return self.av


talabalar = []

talaba_soni = int(input("Talabalr nechta: "))
for i in range(talaba_soni):
    print(f"{1+i} - Talaba haqida malumotlarni kiriting: ")
    talaba = Talaba(input(f"Ismini kiriting: "),
                     input(f"Familiyasini kiriting: "),
                     int(input(f"Matematikadan olgan  bahosi: ")),
                     int(input(f"Dasturlashdan olgan  bahosi: ")),
                     int(input(f"Kimyodan olgan  bahosi: ")))
    talabalar.append(talaba)
for i in range(len(talabalar)):
    print(f"{i+1} talabaning o'rtacha baxosi {talabalar[i].baxo()}")

kottasi = talabalar[i].av
a = 0
for i in range(talaba_soni):
   if talabalar[i].av > kottasi:
       kottasi = talabalar[i].av
       a = i + 1
print(f'{a+1} - o`rindagi talaba eng kata ballni oldi: {talabalar[a].av} Ismi -{talabalar[a].ism} Familiyasi -{talabalar[a].fam}  ')
