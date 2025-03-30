# Car-Insurance

บริษัทประกันแห่งหนึ่งต้องการให้คุณช่วยสร้าง model สำหรับทำนายว่าลูกค้าผู้ซื้อกรมธรรม์ประกันสุขภาพในปีก่อน จะมีความสนใจในกรมธรรม์ตัวใหม่ของบริษัท - ประกันอุบัติเหตุรถยนต์ หรือไม่

หลังจากที่ผู้เอาประกัน ได้ทำการตกลงทำตามข้อสัญญา กับทางบริษัทประกันเป็นที่เรียบร้อยแล้ว ผู้เอาประกัน จะต้องมีการจ่ายค่าตอบแทน (premium) ให้กับผู้รับประกัน ซึ่งก็คือบริษัทประกัน ตามจำนวนเงินในสัญญาภายในกรมธรรม์ (policy) และเมื่อเกิดอุบัติเหตุ บาดเจ็บ เสียทรัพย์ ไปจนถึงเสียชีวิต บริษัทประกัน จะทำการวิเคราะห์เหตุการณ์ และตีค่าออกมาเป็นตัวเงินก่อนจะชดเชยให้กับผู้เอาประกัน หรือผู้รับผลประโยชน์ ตามจำนวนเงินในเงื่อนไขภายในกรมธรรม์

### Data Description

| Variable            | Definition                                                                 |
| ------------------- | -------------------------------------------------------------------------- |
| id                  | Unique ID for the customer                                                 |
| Gender              | Gender of the customer                                                     |
| Age                 | Age of the customer                                                        |
| Driving_License     | 0 : Customer does not have Driving License, <br> 1 : Customer already has Driving License |
| Region_Code         | Unique code for the region of the customer                                 |
| Previously_Insured  | 1 : Customer already has Vehicle Insurance, <br> 0 : Customer doesn't have Vehicle Insurance |
| Vehicle_Age         | Age of the Vehicle                                                         |
| Vehicle_Damage      | 1 : Customer got his/her vehicle damaged in the past. <br> 0 : Customer did not get his/her vehicle damaged in the past. |
| Annual_Premium      | The amount customer needs to pay as premium in the year                    |
| PolicySalesChannel  | Anonymized Code for the channel of outreaching to the customer ie <br> Different Agents, Over Mail, Over Phone, In Person, etc. |
| Vintage             | Number of Days, Customer has been associated with the company             |
| Response            | 1 : Customer is interested, <br> 0 : Customer is not interested           |

### Objective:

- ให้สร้าง model เพื่อทำนายว่าลูกค้าจะสนใจซื้อกรมธรรม์ประกันอุบัติเหตุรถยนต์หรือไม่
- ข้อมูล feature บางตัวมีลักษณะเป็นตัวแปรหมวดหมู่ควรมีการทำตัวแปร dummy
- ควรทำให้ ตัวแปร target class 0 และ 1 ที่จำนวนเท่าๆ กัน (imbalanced dataset)
- จงหาปัจจัยที่มีผลต่อตัวแปร target มากท่ีสุด 3 ลำดับ