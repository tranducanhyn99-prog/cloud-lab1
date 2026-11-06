# Lab 01 Report: Deploy Your First Static Website to the Cloud

| Field | Details |
| :--- | :--- |
| **Student** | **Trần Đức Anh** – **23520001** |
| **Course** | Introduction to Cloud Computing |
| **Lecturer** | Truong Thi Ngoc Phuong |
| **Selected option** | Option B – GitHub Pages |
| **Repository** | `github.com/USERNAME/cloud-lab1` |
| **Public URL** | `https://USERNAME.github.io/cloud-lab1/` |
| **Website title** | My First Cloud Website |

This report contains the deployment evidence (E1–E4) and the written conceptual answers (E5) required by the lab rubric.

---

## E1 – Desktop website
*Full website with student name and ID visible.*

> *(Chèn ảnh chụp toàn bộ trang web trên màn hình máy tính desktop tại đây)*

---

## E2 – Mobile website
*Narrow / mobile viewport (browser F12 &rarr; device toolbar / Responsive view).*

> *(Chèn ảnh chụp giao diện di động / màn hình hẹp tại đây)*

---

## E3 – Hosting dashboard
*GitHub repository &rarr; Settings &rarr; Pages, showing the site is live with green checkmark.*

> *(Chèn ảnh chụp trang cài đặt GitHub Pages trên GitHub thể hiện trạng thái "Your site is live at..." tại đây)*

---

## E4 – HTTPS verification
*Browser address bar showing the public `https://` URL with security lock icon (in an incognito/private window).*

> *(Chèn ảnh chụp thanh địa chỉ trình duyệt ở chế độ ẩn danh thể hiện https:// và biểu tượng ổ khóa an toàn tại đây)*

---

## E5 – Written answers

### Q1. Which platform did you select, and why?
I selected GitHub Pages (Option B). It only needs a free GitHub account and a public repository, so I did not have to buy an AWS account or enter a payment card. I already use Git to manage my coursework, which means publishing is simply a push to the main branch. GitHub Pages also provides an HTTPS address automatically, needs no server setup, and is well suited to a static HTML and CSS site like this one.

### Q2. How does opening index.html locally differ from visiting the deployed HTTPS URL?
Opening `index.html` locally loads the file straight from my own disk through a `file://` address. Only my computer can see it, nothing travels over a network, and it is gone if I turn the machine off or move the file. The deployed HTTPS URL is served by GitHub's web servers instead. Anyone with the link can open it from any device, the browser downloads `index.html`, `style.css` and the image over the internet, and the site stays available all day without my laptop.

### Q3. What is HTTPS, and why is it important?
HTTPS is HTTP running over TLS encryption. It does three jobs: it encrypts the data between the browser and the server so other people on the network cannot read it, it uses a certificate to prove the site really belongs to its domain, and it prevents the content from being changed on the way. It matters because it protects passwords and personal data, builds user trust since browsers warn about plain HTTP, and is required by many modern web features.

### Q4. Does the selected hosting platform fit IaaS, PaaS or SaaS directly? Explain its characteristics.
GitHub Pages fits closest to PaaS, although it is a very limited form of it. I supply only my code; the platform stores it, serves it, renews the HTTPS certificate and handles scaling, so I never manage servers or an operating system. That rules out IaaS, where I would rent and maintain a virtual machine. It is not true SaaS either, because I am deploying my own site rather than just using finished software. It only supports static files, with no server-side code or database.

### Q5. What changes would be needed for authentication or a database?
A static host cannot run server-side code, so I would need a backend. One option is a managed service such as Firebase Authentication, Supabase or AWS Cognito, with the page calling its API over HTTPS using JavaScript. Another is a PaaS such as AWS Amplify, Render or Heroku running a Node.js or Python app with a database like PostgreSQL or DynamoDB. I would hash passwords, use sessions or tokens, keep secrets in environment variables instead of the repository, and configure CORS.
