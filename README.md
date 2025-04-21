# **SurveyBasket API**  

**A Robust RESTful API for Survey Management**  

![.NET Version](https://img.shields.io/badge/.NET-8.0-blue)  
![Database](https://img.shields.io/badge/Database-SQL%20Server-red)  
![License](https://img.shields.io/badge/License-MIT-green)  

SurveyBasket is a **scalable, secure, and high-performance** RESTful API built with **.NET 8.0**, designed to streamline **survey creation, management, and analysis**.  

---

## **✨ Key Features**  

✅ **Survey Management**  
- Create, read, update, and delete surveys, questions, and responses  
- Dynamic survey templates with multiple question types (MCQ, text, rating, etc.)  

✅ **Real-Time Analytics**  
- Live response tracking  
- Automated report generation  

✅ **Security & Access Control**  
- **JWT-based authentication** with refresh tokens  
- **Role-based authorization** (Admin, Survey Creator, Respondent)  

✅ **Performance & Reliability**  
- **Pagination, filtering, and sorting** for large datasets  
- **Rate limiting & caching** (Redis support)  
- **Health checks & logging** (Serilog)  

✅ **Background Processing**  
- Async report generation  
- Audit logging for tracking user actions  

---

## **🛠 Tech Stack**  

| Category        | Technologies Used |  
|----------------|------------------|  
| **Backend**    | .NET 8.0, ASP.NET Core |  
| **Database**   | SQL Server, Entity Framework Core |  
| **Auth**       | JWT, Refresh Tokens |  
| **Logging**    | Serilog |  
| **Caching**    | In-memory, Redis (optional) |  
| **Background Jobs** | Hangfire |  
| **API Docs**   | Swagger (Swashbuckle) |  
| **Validation** | FluentValidation | 
| **Mapping** | Mapster |  
| **SendEmail** | Mailkit |  
| **Error Handling** | Result , OneOf|  

---

## **🚀 Getting Started**  

### **Prerequisites**  
- **.NET 8.0 SDK**  
- **SQL Server 2019+**  
- **Visual Studio 2022 / VS Code**  

### **Installation Steps**  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/mohamedhamed0x/SurveyBasket.git
   ```  

2. **Navigate to the project directory**  
   ```bash
   cd SurveyBasket
   ```  

3. **Restore dependencies**  
   ```bash
   dotnet restore
   ```  

4. **Configure `appsettings.json`**  
   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Your_SQL_Server_Connection_String"
     },
     "Jwt": {
       "Key": "Your_Secret_Key",
       "Issuer": "Your_Issuer",
       "Audience": "Your_Audience"
     }
   }
   ```  

5. **Apply database migrations**  
   ```bash
   dotnet ef database update
   ```  

6. **Run the application**  
   ```bash
   dotnet run
   ```  

---

## **📌 API Usage**  

### **Base URL**  
`https://localhost:5001/api`  

### **Swagger Documentation**  
Available at `/swagger`  

### **Key Endpoints**  

| **Endpoint**          | **Method** | **Description** |  
|----------------------|-----------|----------------|  
| `/api/auth/login`    | `POST`    | User login (JWT token) |  
| `/api/Polls`         | `POST`    | Create a new survey |  
| `/api/Polls`         | `GET`     | Get paginated surveys |  
| `/api/Questions`     | `GET`     | View all Questions |  
| `/api/Questions`     | `POST`    | Create a new Questions |  
| `/me`                | `GET`     | Get User Profile |  

---

## **📂 Project Structure**  

```
SurveyBasket/
├── Controllers/          # API endpoints
├── Services/             # Business logic
├── Contracts/            # DTOs
├── Entities/             # Data models 
├── Persistence/          # Database operations
├── Validators/           # FluentValidation rules
├── Authentication/       # Authentication 
├── BackgroundJobs/       # Async tasks
└── Configurations/       # App settings
```

---

## **🤝 Contributing**  

1. **Fork the repository**  
2. **Create a feature branch** (`git checkout -b feature/your-feature`)  
3. **Commit changes** (`git commit -m "Add your feature"`)  
4. **Push to branch** (`git push origin feature/your-feature`)  
5. **Open a Pull Request**  

---

## **📜 License**  
This project is licensed under the **MIT License**.  

---

## **📩 Contact**  
For questions or collaboration:  
📧 **Email:** mohamedhamedsaleh711@gmail.com  
🐱 **GitHub Issues:** [https://github.com/mohamedhamed0x/SurveyBasket/issues](https://github.com/mohamedhamed0x/SurveyBasket/issues)  

---

### **🌟 Happy Surveying!** 🚀📊  

This version is **fully formatted** for GitHub with:  
✔ **Consistent headers**  
✔ **Proper tables & lists**  
✔ **Code blocks for commands**  
✔ **Emojis for better readability**  
✔ **Clear section separation**  
