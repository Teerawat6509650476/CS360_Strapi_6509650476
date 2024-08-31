## จุดประสงค์ของ Strapi
**Strapi** เป็น Headless CMS ที่ออกแบบมาเพื่อช่วยให้นักพัฒนาสามารถสร้างและจัดการเนื้อหาของเว็บแอปพลิเคชันหรือแอปมือถือได้อย่างมีประสิทธิภาพ โดยที่ Strapi มุ่งเน้นการเป็น CMS ที่ยืดหยุ่นและสามารถปรับแต่งได้ตามความต้องการของผู้ใช้งาน สามารถสร้างเเละปรับเเต่งAPI ได้ง่ายเเละสะดวก




## กรณีการใช้งานของ Strapi

 - Strapi คือ headless CMS ใช้ในการพัฒนา develop websites, mobile applications, eCommerce sites, and APIs
 - Strapi ช่วยให้สร้าง API ได้โดยไม่ต้องรู้ข้อมูลใดๆ เกี่ยวกับ backend or databases
 - Strapi ใช้เพื่อสร้าง backend services ที่ปรับแต่งได้ ยังสามารถรวม Strapi apps เข้ากับ frontend ได้ด้วย
 - Strapi ใช้เพื่อสร้าง websites, mobile applications, เเละ other digital experiences.
 - Strapi เป็น CMS ที่มีความยืดหยุ่น ซึ่ง admin panel เเละ API ของแอปพลิเคชันนั้นขยายได้ โดยอิงตาม plugin system และทุกส่วนสามารถปรับแต่งได้เพื่อให้เหมาะกับ use case




## ส่วนประกอบหลักของ Strapi

**Content Manager** และ **Content-Type Builder** เป็นสององค์ประกอบหลักใน Strapi ที่ช่วยให้การจัดการเนื้อหาและโครงสร้างของข้อมูลเป็นไปได้ง่ายและมีประสิทธิภาพ

**Content Manager:**
 - Content Manager  ให้ผู้ใช้งานสามารถจัดการเนื้อหา ในแอปพลิเคชันของตัวเองได้ง่าย
 - ฟีเจอร์นี้ช่วยให้คุณสามารถสร้าง, แก้ไข, ลบ, และดูรายละเอียดของเนื้อหาที่สร้างขึ้นโดย Content-Type ต่างๆ ได้

 **Content-Type Builder:**
 

 - Content-Type Builder เป็นเครื่องมือที่ช่วยให้คุณสามารถสร้างและจัดการโครงสร้างของข้อมูล (Content Types) ที่จะใช้ใน Strapi โดยไม่ต้องเขียนโค้ด
 - สามารถกำหนดฟิลด์ต่างๆ ที่ต้องการให้แต่ละ Content-Type มี เช่น ชนิดของข้อมูล (text, number, boolean, etc.), ความยาวของข้อมูล, และการตั้งค่าการตรวจสอบความถูกต้อง
 - Content-Type Builder เเบ่งเป็น 2 เเบบ
		 - **Collection Type** เป็นประเภทเนื้อหาที่สามารถจัดการรายการต่างๆ ได้หลายรายการ
		 - **Single Type** เป็นประเภทเนื้อหาที่สามารถจัดการได้เพียงรายการเดียวเท่านั้น




อ้างอิงแหล่งข้อมูล:
https://docs.strapi.io/dev-docs/intro
https://radixweb.com/blog/what-is-strapi#Conclusion
https://docs.strapi.io/user-docs/content-manager
https://docs.strapi.io/user-docs/content-type-builder



## ขั้นตอนการติดตั้งและนำขึ้นให้บริการ

**ก่อนที่จะติดตั้ง Strapi ต้องติดตั้ง** 

 - **NodeJS**   v18 หรือ v20
 - **npm** 		v6 ขึ้นไป

**ขั้นตอนสร้าง Strapi project**

 - เปิด Terminal
 - cd เข้าไปในโฟลเดอร์ที่จะเก็บ Strapi project และใช้คำสั่ง
 ``` bash
 npx create-strapi-app@latest my-project
 ```
 - เมื่อติดตั้งเสร็จจะเข้าไปหน้าสมัคร admin `localhost:1337/admin/register`
 - กรอกข้อมูลหน้าสมัคร
 - สามารถเข้าใช้งานระบบ

**Start Strapi**
``` bash
 npm  run  develop
 ```
อ้างอิงแหล่งข้อมูล:
https://docs.strapi.io/dev-docs/installation/cli
## จุดประสงค์และความสำคัญของ .gitignore

 - .gitignore เป็นไฟล์ที่ใช้ในโปรเจกต์ Git เพื่อระบุไฟล์หรือ directories ที่ไม่ต้องการให้ถูกtracked หรือถูกcommitted ลงใน repository ของ Git ไฟล์ที่ Git ติดตามอยู่แล้วจะไม่ได้รับผลกระทบ
 - **จุดประสงค์หลัก**ของไฟล์ .gitignore มีดังนี้:
		 - **รักษาความสะอาดของ repository:** .gitignore ช่วยให้ repository ไม่มีไฟล์ที่ไม่จำเป็นหรือไฟล์ที่สร้างขึ้นโดยอัตโนมัติจากเครื่องมือหรือโปรแกรมพัฒนาต่างๆ เช่น log files, data files, or user-specific configuration files.
		 -  **เพิ่มความปลอดภัย:** การกำหนดไฟล์ .gitignore ช่วยป้องกัน committing ไฟล์ที่อาจมีข้อมูลสำคัญ เช่น passwords or API keys
		 - **ลดความซับซ้อนในการทำงานร่วมกัน:** ด้วยการใช้ .gitignore ทำให้เพื่อนร่วมทีมไม่ต้องเห็นหรือทำงานกับไฟล์ที่ไม่เกี่ยวข้องกับการพัฒนาจริง ทำให้กระบวนการทำงานร่วมกันเป็นไปอย่างมีประสิทธิภาพมากขึ้น
		 - **รองรับการทำงานที่หลากหลาย:**
เนื่องจากไฟล์ .gitignore สามารถกำหนดค่าเพื่อให้เหมาะสมกับสภาพแวดล้อมการทำงานที่แตกต่างกันได้ ไม่ว่าจะเป็นการพัฒนาแอปพลิเคชันบนระบบปฏิบัติการต่างๆ หรือการใช้ development tools (IDE) ที่แตกต่างกัน


## การใช้งาน .gitignore ในโปรเจกต์ JavaScript
ในโปรเจกต์ JavaScript เมื่อต้องใช้ Node.js และ npm, มีไฟล์และโฟลเดอร์หลายรายการที่มักจะไม่ต้องการให้ถูกติดตามใน Git ตัวอย่างเช่น:

 - **node_modules/:** 
เป็นไดเรกทอรีที่บรรจุ dependencies ของโปรเจกต์ซึ่งสามารถติดตั้งใหม่ได้ผ่าน npm install
 - **npm-debug.log:** 
เป็นไฟล์ที่ถูกสร้างขึ้นเมื่อเกิดข้อผิดพลาดใน npm คำสั่งต่างๆ
 - **dist/ หรือ build/:** 
เป็นโฟลเดอร์ที่เก็บไฟล์ที่สร้างขึ้นจากการ build ซึ่งไม่จำเป็นต้องติดตามใน repository เนื่องจากสามารถสร้างใหม่ได้เสมอ

อ้างอิงแหล่งข้อมูล:
[Git - gitignore Documentation (git-scm.com)](https://git-scm.com/docs/gitignore)
##  Deployment

 -  **Setup AWS Instance**
	 - **Launch **`AWS EC2`** instance**
		 - **Instance Type** : t2.medium
		 - **Operating System** : Ubuntu 24.04
		 - **Security Group Rules**
			 -    Type: `SSH`, Protocol: `TCP`, Port Range `22`, Source: `::/0`
			 - Type: `HTTP`, Protocol: `TCP`, Port Range `80`, Source: `0.0.0.0/0, ::/0`
			 - Type: `HTTPS`, Protocol: `TCP`, Port Range `443`, Source: `0.0.0.0/0, ::/0`
			 - Type: `Custom TCP Rule`, Protocol: `TCP`, Port Range `1337`, Source: `0.0.0.0/0`
	 - SSH เข้าสู่ EC2 Instance ที่สร้าง
	 - ใช้คำสั่ง **`sudo apt update`** เพื่ออัพเดทระบบ
	 - ใช้คำสั่ง **`sudo apt install curl -y`** เพื่อติดตั้ง curl
	 - ติดตั้ง **NodeJS**

	```bash 
	curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -  
	```	 
	```bash 
	curl -fsSL sudo apt install -y nodejs
	```	 
	```bash 
	node -v && npm -v
	```	 
	ตั้งค่า npm global directory
	```bash 
	cd ~
	```	 
	```bash 
	mkdir ~/.npm-global
	```	 
	```bash 
	npm config set prefix '~/.npm-global'
	```	 
	เพิ่ม Path Evironment
	
	```bash 
	sudo nano ~/.profile
	```	 
	```bash 
	export PATH=~/.npm-global/bin:$PATH ใส่ในด้านล่างของไฟล์
	```	 
	```bash 
	source ~/.profile
	```	 
	

	 - ติดตั้ง **Git** `sudo apt install git -y`

	 

 -  **Strapi Project**
	 - ใช้คำสั่ง `git clone <url>` เอาโปรเจ็คจาก GitHub Repository
	 - `cd` เข้าไปในโฟลเดอร์
	 ```bash 
	npm install
	```	 
	```bash 
	NODE_ENV=production npm run build
	```	 
	
	 - สร้างไฟล์ .env ใน Folder ที่เก็บ Strapi Project 
	 - นำไฟล์ .env เข้าในเครื่อง Instance
		 - คัดลอกเนื้อหาในไฟล์ .env 
		 - เข้า terminal
		 - นำเนื้อหาที่คัดลอกมาวาง
		 - นำ NODE_ENV=production ต่อท้ายที่คัดลอกมา
	```bash 
	touch .env
	```	 
	```bash 
	nano .env
	```	 
	```bash 
	npm start
	```	 