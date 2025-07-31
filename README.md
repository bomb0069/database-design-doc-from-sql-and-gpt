# 📘 README: Database Design Prompt Guide for SQL → Markdown Documentation

This guide provides ready-to-use prompts for generating a complete database design documentation from SQL DDL. It outputs a fully structured **Markdown (.md)** file with Mermaid ER diagram and Thai-language explanations — ideal for system documentation or public-facing repositories.

---

## 📐 Output Format

When using the prompts below, ChatGPT will generate a downloadable `.md` file with:

1. ✅ **ER Diagram** at the top in Mermaid syntax (Diagram-as-Code)
2. ✅ Table-by-table schema documentation including:
   - Field name
   - Data type
   - Not Null
   - Primary Key
   - Foreign Key
   - **Thai-language description**
3. ✅ Each table section includes:
   - Table title and name
   - One-line description of the purpose of the table
4. ✅ Final format is Markdown that can be pushed to Git or rendered via static docs

---

## 🇹🇭 Prompt ภาษาไทย

```
จาก SQL ด้านล่างนี้ ขอให้คุณสร้างเอกสาร Database Design Document โดยมีรายละเอียดดังนี้:

1. จัดรูปแบบเป็นไฟล์ Markdown (.md) ที่สามารถดาวน์โหลดได้
2. วาง ER Diagram แบบ Mermaid (Diagram-as-Code) ไว้ด้านบนสุดของไฟล์
3. จากนั้นให้เขียนเอกสารแยกของแต่ละตาราง โดยใช้รูปแบบ:

- หัวตาราง: `## 📑 ตาราง <ชื่อ> – <อธิบายความหมายสั้น ๆ ของตาราง>`
- ตารางรายละเอียดใช้หัว column ดังนี้:
  - ชื่อฟิลด์ (Field)
  - ประเภทข้อมูล (Data Type)
  - ต้องมีข้อมูล (Not Null)
  - Primary Key
  - Foreign Key (ถ้ามี ให้ระบุชื่อตารางที่อ้างอิง)
  - คำอธิบาย (ภาษาไทย)

4. ต้องเขียนให้ครบทุกตารางจาก SQL โดยไม่ข้ามแม้แต่ตารางเดียว
5. อย่าเขียน Mermaid Diagram เพียงอย่างเดียว ต้องมี Table Documentation แยกด้วยทุกครั้ง
6. ตอบกลับในครั้งเดียว และแนบลิงก์ดาวน์โหลด Markdown `.md`

SQL ที่ใช้มีดังนี้:
[วาง SQL ที่นี่]
```

---

## 🌍 Prompt (English)

```
From the SQL schema below, generate a complete database design documentation with the following:

1. Format the entire result as a downloadable `.md` Markdown file
2. At the top, embed an ER Diagram using Mermaid syntax (Diagram-as-Code)
3. After the diagram, document **each table individually**, using this format:
   - Section title: `## 📑 Table <name> – <one-line table purpose in Thai>`
   - Column explanation in a table with headers:
     - Field name
     - Data type
     - Not Null
     - Primary Key
     - Foreign Key (with referenced table, if any)
     - Thai description

4. ⚠️ Do not stop after the Mermaid block — the full field documentation must follow afterward
5. Include **all tables** from the SQL, no skipping
6. Respond in a single message and include a download link for the `.md` file

Here is the SQL:
[insert SQL]
```

---

## 🚀 Example Usage Flow

1. Open ChatGPT
2. Paste one of the prompts above with your SQL script
3. ChatGPT will generate and offer a `.md` download link
4. You can commit that file directly to your Git repository

---

## 📎 Notes

- The Mermaid diagram block should start with \`\`\`mermaid and will render visually in supported Markdown renderers (GitHub, Obsidian, VS Code)
- For PDF/Word generation, add: `กรุณาสร้างไฟล์ .docx ด้วย` or `Please generate a .docx version too`

---

Happy documenting! ✍️
