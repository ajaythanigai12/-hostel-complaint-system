# Hostel Complaint System

Dealing with hostel issues is annoying enough without having to fight a clunky reporting system. I put this simple, responsive web app together to give students a clean, straightforward way to log their complaints. 

The interface is styled with Tailwind CSS so it works smoothly whether a student is using a phone or a laptop. Instead of setting up a traditional server, I built the backend using a serverless AWS stack, which keeps things incredibly fast, scalable, and completely maintenance-free.

---

## 🛠️ The Tech Stack

* **Frontend:** Just clean HTML5, Tailwind CSS, and vanilla JavaScript.
* **Backend Integration:** Connected straight to an **AWS API Gateway** REST endpoint.
* **Serverless Compute:** An **AWS Lambda** function handles the backend logic when a form is submitted.
* **Database:** **Amazon DynamoDB** securely stores all the incoming complaints in a NoSQL table.

---

## 🚀 How it Works under the Hood

1. **Quick Validation:** When someone fills out the form, plain JavaScript validates the inputs on the fly (and right when they click away from a field) so nobody sends blank entries by mistake.
2. **Going Serverless:** Once the form is submitted, the frontend kicks off a `fetch` request to **API Gateway**. 
3. **Processing & Storage:** API Gateway immediately passes the data to an **AWS Lambda** function, which processes the request and writes the complaint details directly into **DynamoDB**.
4. **Clean User Experience:** The UI updates instantly with a success message without forcing the page to refresh.
