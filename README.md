# 16-Bit Processor Datapath Design (Logisim Project)

This project was developed as part of the **Computer Organization and Architecture** course. A simple 16-bit processor architecture capable of executing basic instructions was designed using classic Logisim software.

## 📌 Project Overview

The processor supports the following instructions:

- `SUBI` – Subtracts an immediate value from a register.
- `ORI` – Performs a bitwise OR operation with a register and an immediate.
- `STR` – Stores the content of a register into memory.
- `BNE` – Branches to a new instruction if two registers are not equal.

The processor follows a classic 5-stage architecture:
1. Fetch  
2. Decode  
3. Execute  
4. Memory  
5. Write Back  

## ⚙️ Architectural Components

- **Program Counter (PC):** Holds the address of the current instruction.
- **Instruction Memory:** Stores the instruction set.
- **Instruction Decoder:** Splits instructions into opcode, registers, and immediate fields.
- **Register File:** Contains 8 general-purpose 16-bit registers.
- **ALU:** Performs operations like SUBI and ORI.
- **Data Memory:** Stores data using the STR instruction.
- **Control Unit:** Generates control signals such as ALUOp, RegWrite, MemWrite, Branch.
- **MUXes:** Used to select between register or immediate values for ALU and branching.

## 🧠 Instruction Formats

### Arithmetic/Logic Instructions
```

Opcode (5) | Rd (3) | Rs (3) | Immediate (5)

```
**SUBI Rd, Rs, #imm**  
**ORI  Rd, Rs, #imm**

### Memory Instruction
```

Opcode (5) | Rt (3) | Ra (3) | Offset (5)

```
**STR Rt, [Ra, #offset]**

### Branch Instruction
```

Opcode (5) | Rs (3) | Rt (3) | Label (5)

```
**BNE Rs, Rt, #label**

## 🧪 Testing and Simulation

- Registers were manually initialized.
- Instructions were executed step-by-step using clock pulses.
- The proper execution of each instruction was verified.
- Branching was based on the zero flag result from the ALU.

## 📁 Project Files

- `bit16.circ` – Logisim circuit file  
- `README.md` – This documentation file  
![Proje Genel Hatları](https://github.com/user-attachments/assets/6bbffc21-9163-492f-861f-42278a2293a0)


---


# 16-Bit İşlemci Veri Yolu Tasarımı (Logisim Projesi)

Bu proje, **Bilgisayar Organizasyonu ve Mimarisi** dersi kapsamında gerçekleştirilmiştir. Klasik Logisim yazılımı kullanılarak temel komutları çalıştırabilen, 16-bit genişliğinde bir işlemci mimarisi tasarlanmıştır.

## 📌 Proje Özeti

Projede desteklenen komutlar şunlardır:

- `SUBI` – Register ile immediate değeri çıkartır.
- `ORI` – Register ile immediate değeri bit düzeyinde VEYA (OR) işlemi yapar.
- `STR` – Register'daki veriyi belleğe yazar.
- `BNE` – İki register eşit değilse dallanma yapar.

İşlemci mimarisi klasik 5 aşamalı yapıdadır:
1. Fetch
2. Decode
3. Execute
4. Memory
5. Write Back

## ⚙️ Mimari Bileşenler

- **Program Counter (PC):** Komut adresini tutar.
- **Instruction Memory:** Komutları barındırır.
- **Instruction Decoder:** Komutu opcode ve alanlara ayırır.
- **Register File:** 8 adet 16-bit yazmaç içerir.
- **ALU:** SUBI, ORI işlemlerini gerçekleştirir.
- **Data Memory:** STR komutu ile veriyi yazar.
- **Control Unit:** Komutlara göre kontrol sinyalleri üretir.
- **MUX'lar:** ALU ve dallanma kaynaklarını seçmekte kullanılır.

## 🧠 Komut Formatları

### Aritmetik/Mantıksal Komutlar
```

Opcode (5) | Rd (3) | Rs (3) | Immediate (5)

```
**SUBI Rd, Rs, #imm**  
**ORI  Rd, Rs, #imm**

### Bellek Komutu
```

Opcode (5) | Rt (3) | Ra (3) | Offset (5)

```
**STR Rt, [Ra, #offset]**

### Dallanma Komutu
```

Opcode (5) | Rs (3) | Rt (3) | Label (5)

```
**BNE Rs, Rt, #label**

## 🧪 Test ve Simülasyon

- Yazmaçlara başlangıç değerleri elle yüklendi.
- Clock darbesi ile komutlar adım adım çalıştırıldı.
- Komutların doğru şekilde yürütüldüğü gözlemlendi.
- Dallanma kontrolleri sıfır bayrağına göre çalıştırıldı.

## 📁 Proje Dosyaları

- `bit16.circ` – Logisim devre dosyası
- `README.md` – Bu tanıtım dosyası
![Proje Genel Hatları](https://github.com/user-attachments/assets/6bbffc21-9163-492f-861f-42278a2293a0)
