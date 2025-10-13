# 📋 Template Prompt สำหรับสร้างเอกสาร SRS
## Software Requirements Specification Template Guide

### 🎯 **Main Prompt สำหรับสร้าง SRS Document**

```
Create a comprehensive Software Requirements Specification (SRS) document following IEEE/ISO/IEC 29148:2018 standard for [ระบบที่ต้องการ].

Document Structure Required:
1. บทนำ (Introduction) - วัตถุประสงค์, ขอบเขต, ผู้อ่าน, อ้างอิง
2. ภาพรวมระบบ (Overall Description) - มุมมองผลิตภัณฑ์, ฟังก์ชันหลัก, คุณลักษณะผู้ใช้, สภาพแวดล้อม
3. ข้อกำหนดระบบ (System Requirements) - ข้อกำหนดการทำงาน, ไม่ใช่การทำงาน, ส่วนติดต่อผู้ใช้
4. การตรวจสอบ (Verification) - เกณฑ์การทดสอบ, วิธีการตรวจสอบ
5. ภาคผนวก (Appendices) - แผนภาพ, โมเดล, เอกสารอ้างอิง

Language: Thai with English technical terms
Format: Markdown with clear hierarchy
Standards: IEEE/ISO/IEC 29148:2018 compliance
Tone: Professional, technical, suitable for hospital/government organization
Length: Comprehensive (500+ lines minimum)
Include: Stakeholder requirements, functional requirements, non-functional requirements, use cases, system constraints
```

---

## 🏗️ **Prompt Templates แยกตามส่วน**

### **1. การวิเคราะห์ระบบ (System Analysis)**

```
Analyze and document the following system: [ชื่อระบบ]

Required Analysis:
- Stakeholder identification and requirements
- Business process analysis
- Current system limitations
- Proposed solution benefits
- Risk assessment and mitigation
- Integration requirements with existing systems

Context: [บริบทองค์กร เช่น โรงพยาบาล, หน่วยงานราชการ]
Standards: IEEE 29148:2018
Output: Thai language with technical English terms
Focus: Comprehensive stakeholder analysis and business requirements
```

### **2. ข้อกำหนดการทำงาน (Functional Requirements)**

```
Create detailed functional requirements for [ชื่อระบบ] following IEEE 29148:2018 standard.

Structure Required:
- FR-01 to FR-XX format with unique identifiers
- User story format: "ในฐานะ [ผู้ใช้] ฉันต้องการ [ฟังก์ชัน] เพื่อที่ [วัตถุประสงค์]"
- Input/Output specifications
- Business rules and validation criteria
- Priority levels (High/Medium/Low)
- Acceptance criteria for each requirement

System Type: [เช่น Healthcare, Education, Government]
User Groups: [กลุ่มผู้ใช้หลัก]
Language: Thai with English technical terms
Format: Structured requirements with traceability
```

### **3. ข้อกำหนดที่ไม่ใช่การทำงาน (Non-Functional Requirements)**

```
Define comprehensive non-functional requirements for [ชื่อระบบ] system.

Categories to Cover:
- Performance Requirements (response time, throughput, capacity)
- Security Requirements (authentication, authorization, data protection)
- Usability Requirements (user experience, accessibility)
- Reliability Requirements (availability, fault tolerance)
- Compatibility Requirements (browsers, devices, OS)
- Compliance Requirements (regulations, standards)
- Scalability and Maintainability

Context: [ประเภทองค์กร]
Standards: IEEE 29148:2018, relevant industry standards
Language: Thai with technical English terms
Format: Measurable and testable requirements
Include: Specific metrics and acceptance criteria
```

### **4. การออกแบบส่วนติดต่อผู้ใช้ (UI/UX Requirements)**

```
Create user interface and user experience requirements for [ชื่อระบบ].

Requirements Include:
- User interface guidelines and standards
- Accessibility requirements (WCAG 2.1 compliance)
- Responsive design specifications
- User interaction patterns
- Navigation requirements
- Visual design principles
- Mobile-first considerations
- Usability testing criteria

Target Users: [กลุ่มเป้าหมาย เช่น ผู้สูงอายุ, เจ้าหน้าที่การแพทย์]
Platforms: [Web, Mobile, Desktop applications]
Language: Thai interface with English technical documentation
Standards: WCAG 2.1, responsive design principles
```

---

## 🎨 **Visual Documentation Prompts**

### **5. System Architecture Diagrams**

```
Create comprehensive system architecture documentation for [ชื่อระบบ].

Diagrams Required:
- System Context Diagram (showing external entities)
- Component Architecture (system modules and relationships)
- Data Flow Diagrams (Level 0, Level 1)
- Entity Relationship Diagram (database design)
- Use Case Diagrams (user interactions)
- Deployment Diagram (infrastructure layout)

Format: DrawIO (.drawio) files
Style: Professional, clean, corporate healthcare/government aesthetic
Colors: Blue-based professional palette
Standards: UML notation where applicable
Language: Thai labels with English technical terms
```

### **6. UI/UX Mockups and Wireframes**

```
Design comprehensive UI/UX mockups and wireframes for [ชื่อระบบ].

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
Tools: DrawIO format for easy editing
Colors: Consistent with brand guidelines
```

---

## 📊 **Documentation Standards**

### **7. Quality Assurance Prompts**

```
Create quality assurance and testing documentation for [ชื่อระบบ] SRS.

Documentation Include:
- Verification and validation criteria
- Test case specifications
- User acceptance testing procedures
- Performance testing requirements
- Security testing protocols
- Compliance verification methods
- Risk assessment and mitigation strategies

Standards: IEEE 29148:2018 verification requirements
Format: Structured testing documentation
Language: Thai with technical English terms
Scope: Complete system testing coverage
```

### **8. Project Management Integration**

```
Create project management and implementation documentation for [ชื่อระบบ].

Include:
- Project timeline and milestones
- Resource allocation requirements
- Risk management plan
- Change management procedures
- Stakeholder communication plan
- Budget considerations (if applicable)
- Success metrics and KPIs

Context: [ประเภทองค์กร]
Standards: Project management best practices
Format: Structured project documentation
Integration: Links to technical requirements
```

---

## 🎯 **Usage Instructions**

### **วิธีการใช้ Template นี้:**

1. **เลือก Prompt หลัก** - ใช้ Main Prompt เป็นพื้นฐาน
2. **ปรับแต่งรายละเอียด** - แทนที่ [ชื่อระบบ] และข้อมูลเฉพาะ
3. **เพิ่มบริบท** - ใส่ข้อมูลองค์กร สภาพแวดล้อม และข้อจำกัด
4. **ระบุมาตรฐาน** - เลือกมาตรฐานที่เหมาะสม (IEEE, ISO, etc.)
5. **กำหนดขอบเขต** - ชัดเจนในเรื่องสิ่งที่อยู่ในและนอกขอบเขต

### **ตัวอย่างการปรับแต่ง:**

```
Original: [ชื่อระบบ]
Replace with: ระบบจัดการข้อมูลผู้ป่วยโรคเบาหวาน (Diabetes Management System)

Original: [บริบทองค์กร]
Replace with: โรงพยาบาลศูนย์ จังหวัดเชียงใหม่ ที่มีผู้ป่วยโรคเบาหวาน 500+ คน

Original: [กลุ่มผู้ใช้หลัก]
Replace with: ผู้ป่วยโรคเบาหวาน, แพทย์ผู้เชี่ยวชาญ, พยาบาล, เภสัชกร
```

### **Checklist สำหรับ SRS ที่สมบูรณ์:**

- ✅ ปฏิบัติตามมาตรฐาน IEEE/ISO/IEC 29148:2018
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

**🔄 อัพเดท:** เวอร์ชัน 1.0 - ตุลาคม 2568