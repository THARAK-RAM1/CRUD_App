# 📝 Todo App — .NET MAUI + ASP.NET Core Web API

This project is a simple **Todo List App** with:

- 🌐 A **backend** built using **ASP.NET Core Web API**
- 📱 A **cross-platform frontend** using **.NET MAUI**

It supports adding, editing, and deleting todo items, synced with a RESTful API.

---

## 📁 Project Structure

TodoApp/
├── TodoApi/ # ASP.NET Core Web API backend
└── TodoMauiApp/ # .NET MAUI frontend (Android)

yaml
Copy
Edit

---

## ⚙️ Prerequisites

Ensure the following tools are installed:

| Tool              | Version / Info                         |
|-------------------|----------------------------------------|
| .NET SDK          | .NET 8 or later                        |
| Visual Studio     | 2022/2023 with .NET MAUI + ASP.NET     |
| Android Emulator  | API Level 29 or higher recommended     |
| Git               | For version control and GitHub         |

---

## 🧪 Step 1: Load the Project in Visual Studio

1. Open **Visual Studio**
2. Go to **File → Open → Project/Solution**
3. Navigate to the root folder and open:
   - The solution `.sln` file (if available), **or**
   - Open both projects individually:
     - `TodoWebAPI/TodoWebAPI.csproj`
     - `TodoMauiApp/TodoMauiApp.csproj`

---

## ▶️ Step 2: Run the Backend

1. Press `F5` or click the **Run** button.
2. The backend will start and open Swagger UI at:

https://localhost:5142/swagger

markdown
Copy
Edit

3. Test endpoints:
- `GET /api/todo`
- `POST /api/todo`
- `DELETE /api/todo/{id}`

✅ This confirms that the backend is running properly.

---

## 📱 Step 3: Run the Frontend (MAUI Android App)

### 3.1 Setup

- Set `TodoMauiApp` as the **Startup Project** in Visual Studio.
- Open `MainPage.xaml.cs` and confirm the base URL is set as:

```csharp
private const string BaseUrl = "https://10.0.2.2:5142/api/todo";
Note: 10.0.2.2 is used by Android emulators to access the localhost of the development machine.

3.2 Run
Select an Android Emulator (e.g., Pixel API 30) from the device dropdown.

Press F5 or click Run.

The app will deploy and open in the emulator.

🧪 Step 4: Test the App
Feature	How-To
✅ Add Task	Enter a task name in the input field → Click “Add Task”
📃 View Tasks	Added tasks appear in the list below
❌ Delete Task	Tap the red ❌ icon next to the task
