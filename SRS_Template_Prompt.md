# 📋 Template Prompt สำหรับสร้างเอกสาร SRS (Parametric)
## Software Requirements Specification Template Guide

ส่วนนี้ออกแบบให้แก้ไขค่าครั้งเดียวและใช้ซ้ำได้ทุกส่วนด้วยตัวแปรรูปแบบ ${VAR} เพื่อความสะดวกในการสร้าง SRS สำหรับระบบใหม่

## Variables (แก้ไขเฉพาะส่วนนี้)

- ${SYSTEM_NAME}: ระบบให้เลือดปลอดภัย (Blood Safety by QR Code)
- ${SHORT_NAME}: BloodSafety
- ${ORG_CONTEXT}: โรงพยาบาลอ่างทอง (ATH Hospital)
- ${DOMAIN}: Healthcare / Blood Bank Safety
- ${PRIMARY_TECH}: PHP, MySQL, LIFF/LINE, QR Code
- ${DATA_SOURCES}: ./data, ./temp (ใช้ DDL/SQL, source code, และเอกสารในที่เก็บนี้เป็นหลัก)
- ${STANDARD}: IEEE/ISO/IEC 29148:2018
- ${LANG}: Thai with English technical terms
- ${TONE}: Professional, technical, suitable for hospital/government

คำแนะนำ: หากสร้าง SRS สำหรับระบบใหม่ ให้คัดลอกไฟล์นี้ เปลี่ยนค่าตัวแปรด้านบน แล้วใช้งาน prompt ทั้งหมดด้านล่างโดยไม่ต้องแก้ไขซ้ำในแต่ละส่วน

### 🎯 **Main Prompt สำหรับสร้าง SRS Document**

```
Create a comprehensive Software Requirements Specification (SRS) document following ${STANDARD} for ${SYSTEM_NAME}.

Document Structure Required:
1. บทนำ (Introduction) - วัตถุประสงค์, ขอบเขต, ผู้อ่าน, อ้างอิง
2. ภาพรวมระบบ (Overall Description) - มุมมองผลิตภัณฑ์, ฟังก์ชันหลัก, คุณลักษณะผู้ใช้, สภาพแวดล้อม
3. ข้อกำหนดระบบ (System Requirements) - ข้อกำหนดการทำงาน, ไม่ใช่การทำงาน, ส่วนติดต่อผู้ใช้
4. การตรวจสอบ (Verification) - เกณฑ์การทดสอบ, วิธีการตรวจสอบ
5. ภาคผนวก (Appendices) - แผนภาพ, โมเดล, เอกสารอ้างอิง

Language: Thai with English technical terms
Format: Markdown with clear hierarchy
Standards: ${STANDARD} compliance
Tone: ${TONE}
Length: Comprehensive (500+ lines minimum)
Include: Stakeholder requirements, functional requirements, non-functional requirements, use cases, system constraints

Repository context and evidence-based writing:
- Use artifacts in ${DATA_SOURCES} as primary references
	- SQL DDL in ./data/*.sql to infer actual database structure and constraints
	- Existing code and assets in ./temp/** to understand implemented flows/UI
	- Use filenames and fields explicitly in requirements where relevant
- State assumptions clearly when the artifacts do not cover a detail
```

---

## 🏗️ **Prompt Templates แยกตามส่วน**

### **1. การวิเคราะห์ระบบ (System Analysis)**

```
Analyze and document the following system: ${SYSTEM_NAME}

Required Analysis:
- Stakeholder identification and requirements
- Business process analysis
- Current system limitations
- Proposed solution benefits
- Risk assessment and mitigation
- Integration requirements with existing systems

Context: ${ORG_CONTEXT}
Standards: ${STANDARD}
Output: ${LANG}
Focus: Comprehensive stakeholder analysis and business requirements
Use evidence from ${DATA_SOURCES}: map processes to real tables/fields and existing code modules.
```

### **2. ข้อกำหนดการทำงาน (Functional Requirements)**

```
Create detailed functional requirements for ${SYSTEM_NAME} following ${STANDARD}.

Structure Required:
- FR-01 to FR-XX format with unique identifiers
- User story format: "ในฐานะ [ผู้ใช้] ฉันต้องการ [ฟังก์ชัน] เพื่อที่ [วัตถุประสงค์]"
- Input/Output specifications
- Business rules and validation criteria
- Priority levels (High/Medium/Low)
- Acceptance criteria for each requirement

System Type: ${DOMAIN}
User Groups: ผู้บริจาคเลือด, เจ้าหน้าที่ธนาคารเลือด, เจ้าหน้าที่หอผู้ป่วย, ผู้ดูแลระบบ (ปรับตามจริง)
Language: ${LANG}
Format: Structured requirements with traceability
Refer to SQL columns and constraints from ./data/*.sql and to code flows in ./temp when applicable.
```

### **3. ข้อกำหนดที่ไม่ใช่การทำงาน (Non-Functional Requirements)**

```
Define comprehensive non-functional requirements for ${SYSTEM_NAME} system.

Categories to Cover:
- Performance Requirements (response time, throughput, capacity)
- Security Requirements (authentication, authorization, data protection)
- Usability Requirements (user experience, accessibility)
- Reliability Requirements (availability, fault tolerance)
- Compatibility Requirements (browsers, devices, OS)
- Compliance Requirements (regulations, standards)
- Scalability and Maintainability

Context: ${ORG_CONTEXT}
Standards: ${STANDARD}, relevant industry standards
Language: ${LANG}
Format: Measurable and testable requirements
Include: Specific metrics and acceptance criteria
```

### **4. การออกแบบส่วนติดต่อผู้ใช้ (UI/UX Requirements)**

```
Create user interface and user experience requirements for ${SYSTEM_NAME}.

Requirements Include:
- User interface guidelines and standards
- Accessibility requirements (WCAG 2.1 compliance)
- Responsive design specifications
- User interaction patterns
- Navigation requirements
- Visual design principles
- Mobile-first considerations
- Usability testing criteria

Target Users: ผู้บริจาคเลือด, เจ้าหน้าที่ (ปรับตามจริง)
Platforms: Web, Mobile/LIFF (ถ้ามี)
Language: Thai interface with English technical documentation
Standards: WCAG 2.1, responsive design principles
```

---

## 🎨 **Visual Documentation Prompts**

### **5. System Architecture Diagrams**

```
Create comprehensive system architecture documentation for ${SYSTEM_NAME}.

Diagrams Required:
- System Context Diagram (showing external entities)
- Component Architecture (system modules and relationships)
- Data Flow Diagrams (Level 0, Level 1)
- Entity Relationship Diagram (database design)
- Use Case Diagrams (user interactions)
- Deployment Diagram (infrastructure layout)

Format: DrawIO (.drawio) files stored under ./docs/diagrams/${SHORT_NAME}/
Style: Professional, clean, corporate healthcare/government aesthetic
Colors: Blue-based professional palette
Standards: UML notation where applicable
Language: Thai labels with English technical terms
```

### **6. UI/UX Mockups and Wireframes**

```
Design comprehensive UI/UX mockups and wireframes for ${SYSTEM_NAME}.

Components Required:
For Mobile Applications:
- Main menu/dashboard
- Registration/login flows
- Primary function screens
- Navigation patterns
- Error handling displays

For Web Applications:
- Dashboard layouts
- Data entry forms
- Reporting interfaces
- Administrative panels
- User management screens

Style: Professional, accessible design
Target Users: [ระบุกลุ่มผู้ใช้]
Standards: Mobile-first, responsive design
Tools: DrawIO format for easy editing; save in ./docs/diagrams/${SHORT_NAME}/ as `mockup-${SHORT_NAME}-*.drawio`
Colors: Consistent with brand guidelines
```

---

## 📊 **Documentation Standards**

### **7. Quality Assurance Prompts**

```
Create quality assurance and testing documentation for ${SYSTEM_NAME} SRS.

Documentation Include:
- Verification and validation criteria
- Test case specifications
- User acceptance testing procedures
- Performance testing requirements
- Security testing protocols
- Compliance verification methods
- Risk assessment and mitigation strategies

Standards: ${STANDARD} verification requirements
Format: Structured testing documentation
Language: ${LANG}
Scope: Complete system testing coverage
```

### **8. Project Management Integration**

```
Create project management and implementation documentation for ${SYSTEM_NAME}.

Include:
- Project timeline and milestones
- Resource allocation requirements
- Risk management plan
- Change management procedures
- Stakeholder communication plan
- Budget considerations (if applicable)
- Success metrics and KPIs

Context: ${ORG_CONTEXT}
Standards: Project management best practices
Format: Structured project documentation
Integration: Links to technical requirements
```

---

## 🎯 **Usage Instructions**

### **วิธีการใช้ Template นี้:**

1. **เลือก Prompt หลัก** - ใช้ Main Prompt เป็นพื้นฐาน
2. **ปรับแต่งรายละเอียด** - แก้ไขเฉพาะค่าที่ส่วน Variables ด้านบน ไม่ต้องแก้ใน prompt ย่อย
3. **เพิ่มบริบท** - ใส่ข้อมูลองค์กร สภาพแวดล้อม และข้อจำกัด
4. **ระบุมาตรฐาน** - เลือกมาตรฐานที่เหมาะสม (IEEE, ISO, etc.)
5. **กำหนดขอบเขต** - ชัดเจนในเรื่องสิ่งที่อยู่ในและนอกขอบเขต

### **ตัวอย่างการปรับแต่ง:**

```
Original: [ชื่อระบบ]
Replace with: ระบบจัดการข้อมูลผู้ป่วยโรคเบาหวาน (Diabetes Management System)

Original: [บริบทองค์กร]
Replace with: โรงพยาบาลทั่วไป จังหวัดอ่างทอง ที่มีผู้ป่วยโรคเบาหวาน 300+ คน

Original: [กลุ่มผู้ใช้หลัก]
Replace with: ผู้ป่วยโรคเบาหวาน, แพทย์ผู้เชี่ยวชาญ, พยาบาล, เภสัชกร
```

### **Checklist สำหรับ SRS ที่สมบูรณ์:**

- ✅ ปฏิบัติตามมาตรฐาน ${STANDARD}
- ✅ ครอบคลุมทุกกลุ่มผู้มีส่วนได้ส่วนเสีย
- ✅ ข้อกำหนดสามารถตรวจสอบได้ (Verifiable)
- ✅ ข้อกำหนดสามารถติดตาม (Traceable)
- ✅ ไม่มีข้อกำหนดที่ขัดแย้งกัน
- ✅ ครอบคลุมการทำงานและไม่ใช่การทำงาน
- ✅ มีการประเมินความเสี่ยงและการจัดการ
- ✅ เหมาะสมกับบริบทและวัฒนธรรมองค์กร
- ✅ ใช้ภาษาไทยที่ชัดเจนผสมศัพท์เทคนิคภาษาอังกฤษ
- ✅ มีแผนภาพและ mockups ประกอบที่เหมาะสม

---

## 🏥 **Templates สำหรับ Domain เฉพาะ**

### **Healthcare Systems**
```
Additional Context for Healthcare SRS:
- PDPA compliance requirements
- Medical data security standards
- Healthcare workflow integration
- Patient safety considerations
- Medical device integration
- Electronic health record compatibility
- Clinical decision support requirements
- Audit trail and logging needs
```

### **Government Systems**
```
Additional Context for Government SRS:
- Digital Government policy compliance
- Accessibility standards (Universal Design)
- Multi-language support requirements
- Security clearance levels
- Government cloud deployment
- Inter-agency data sharing protocols
- Citizen service delivery standards
- Transparency and accountability features
```

### **Educational Systems**
```
Additional Context for Educational SRS:
- Learning management system integration
- Student information system compatibility
- Academic calendar alignment
- Multi-role access (students, teachers, parents, administrators)
- Assessment and grading requirements
- Communication and notification systems
- Digital content management
- Progress tracking and analytics
```

---

**📝 บันทึก:** Template นี้ใช้เป็นแนวทางในการสร้าง SRS ที่มีคุณภาพ ควรปรับแต่งให้เหมาะสมกับบริบทและความต้องการเฉพาะของแต่ละโครงการ

### 📁 Diagram scaffolding

เมื่อสร้าง SRS ใหม่ ให้สร้างโฟลเดอร์ภาพประกอบไว้ที่ `./docs/diagrams/${SHORT_NAME}/` และสร้างไฟล์ตามรายการนี้ (เปิด/แก้ไขด้วย diagrams.net):
- context-${SHORT_NAME}.drawio
- dfd-l0-${SHORT_NAME}.drawio
- dfd-l1-${SHORT_NAME}.drawio
- architecture-${SHORT_NAME}.drawio
- erd-${SHORT_NAME}.drawio
- usecases-${SHORT_NAME}.drawio
- deployment-${SHORT_NAME}.drawio
- mockup-${SHORT_NAME}-welcome.drawio
- mockup-${SHORT_NAME}-checkout.drawio
- mockup-${SHORT_NAME}-report.drawio

การอ้างอิงข้อมูล: ใช้ไฟล์ใน ${DATA_SOURCES} เป็นหลัก เช่น `./data/*.sql` สำหรับ schema และ `./temp/**` สำหรับ flow/UI ที่มีอยู่แล้ว

**🔄 อัพเดท:** เวอร์ชัน 2.0 - ตุลาคม 2568 (Parametric + repo-aware)