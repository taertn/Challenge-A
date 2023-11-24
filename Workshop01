#1.จงเขียนโปรแกรมด้วย Python ชื่อไฟล์ workshop01.py
#ก.เขียนโปรแกรมรับประโยคเป็นข้อความภาษาอังกฤษจากผู้ใช้ 1  ประโยค
#ข. ให้แสดงผลลัพธ์ออกมาว่าประโยคนั้นประกอบด้วยคําทั้งหมดรวมกี่คํา
#ค.มีคําที่ซ้ํากันรวมกี่คํา คําว่าอะไรบ้างง.แต่ละคําที่ซ้ํา ซ้ํากันกี่ครั้ง
#ทั้งนี้ โปรแกรมต้องไม่มีข้อผิดพลาดเกิดขึ้นขณะโปรแกรมทํางานหรือขณะ
 
 
 
def count_and_check_duplicate_words(sentence):
    # แปลงประโยคเป็นตัวพิมพ์เล็กทั้งหมดเพื่อไม่ให้คำต่างกันเนื่องจากตัวพิมพ์ใหญ่-เล็ก
    sentence = sentence.lower()
 
    # แยกคำในประโยค
    words = sentence.split()
 
    # สร้างตัวแปรสำหรับเก็บคำที่เจอแล้ว
    seen_words = set()
 
    # สร้างตัวแปรนับคำ
    word_count = {}
 
    # สร้างตัวแปรสำหรับเก็บคำที่ซ้ำกัน
    duplicate_words = []
 
    for word in words:
        # ถ้าคำนี้ยังไม่เคยพบมาก่อน
        if word not in seen_words:
            # เพิ่มคำลงในเซตของคำที่เจอแล้ว
            seen_words.add(word)
 
            # เพิ่มหรือสร้างค่าให้กับตัวแปรนับคำ
            word_count[word] = word_count.get(word, 0) + 1
        else:
            # ถ้าคำซ้ำกัน
            duplicate_words.append(word)
 
    return word_count, duplicate_words
 
# รับข้อความจากผู้ใช้
user_sentence = input("กรุณากรอกประโยค: ")
 
# เรียกใช้ฟังก์ชันและแสดงผลลัพธ์
result, duplicates = count_and_check_duplicate_words(user_sentence)
 
# แสดงผลลัพธ์
print('+'*50)
print(f'ป้อนข้อความ : {user_sentence}')
print('+'*50)
print(f'มีคำทั้งหมด {len(result)} คำ')
print(f'มีคำที่ซ้ำกันรวม {len(duplicates)} คำ')
print(f'คือ {", ".join(duplicates)}')
print('+'*50)
 
# แสดงคำที่ซ้ำและจำนวนครั้งที่ปรากฏ
for duplicate_word in duplicates:
    count = result[duplicate_word]
    print(f'คำว่า {duplicate_word} ซ้ำกัน {count} ครั้ง')
 
print('+'*50)