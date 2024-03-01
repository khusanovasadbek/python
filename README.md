#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Dasturlash asoslari

#20-dars: FUNKSIYADAN QIYMAT QAYTARISH

@author: asadbek
"""
def f_malumotlar(ism, familiya, t_yil, t_joy, tel_raqam = None, email = None):
   """Foydanaluvchidan ismi, familiyasi, tug'ilgan yili, tug'ilgan joyi, email manzili va 
   telefon raqamini qabul qilib, lug'at ko'rinishida qaytaruvchi funksiya"""
   malumotlar = {
        'ism':ism,
        'familiya':familiya,
        't_yil':t_yil,
        'yosh':2024 - t_yil,
        't_joy':t_joy,
        'tel_raqam':tel_raqam,
        'email':email
        }
   return (malumotlar)

print("O'zingiz haqingizda ma'lumotni kiriting: ")
malumot = []
while True:
    ism = input("\nIsmingizni kiriting: ")
    familiya=input("Familiyagizni kiriting: ")
    t_yil = int(input("Tug'ilgan yiligizni kiriting: "))
    t_joy = input("Tug'ilgan joyigizni kiriting: ")
    tel_raqam =int(input("Tel rqamingizni kiriting: "))
    email = input("Emailgizni kiriting: ")
    
    malumot.append(f_malumotlar(ism, familiya, t_yil, t_joy, tel_raqam, email))  
    
    javob =input("Yana ma'lumot qoshasizmi? (yes/no).")
    if javob =='no':
        break
    
print("Foydalanuvchinging ma'lumotlari: ")
for malumotlar in malumot:
    print(
        f"{malumotlar['ism'].title()} {malumotlar['familiya'].title()}, "
        f"{malumotlar['yosh']} yoshda, Tug'ulgan joyi :{malumotlar['t_joy']} \ntelefoni: {malumotlar['tel_raqam']}"
        f"\nEmial: {malumotlar['email']}" 
        ) 
        
