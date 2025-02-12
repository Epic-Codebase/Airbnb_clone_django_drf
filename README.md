# 🏡 Airbnb Clone API Backend 🛠

Welcome to the Airbnb Clone API Backend, a 📈 scalable and 🔒 secure backend solution for an Airbnb-like 🏠 application, built using Django Rest Framework (DRF) 🧑‍💻. This project provides a ✨ feature-rich ✨ API to manage properties, bookings, user authentication, and more.

## 🔍 Features

- **🔐 User Authentication**: Secure 🚀 user registration & login.
- **📝 Property Categorization**: Classify properties as 🏖️ Beach, 🏡 Villas, 🏠 Cabins, and 🏰 Tiny Homes.
- **📚 Property Management**: 💼 Create, update & manage properties.
- **📅 Booking System**: Book properties 🏨 for specific date ranges.
- **🛋️ User Listings**: View 🏢 hosted properties.
- **🔍 Property Search**: Search 🔎 based on location, dates & guests.
- **💬 Real-time Chat**: Chat 🛡️ with property owners after booking.

## 📚 Project Structure

```
Airbnb_clone_django_drf/
├── djangobnb_backend/
│   ├── djangobnb_backend/  # ⚙ Django project settings
│   ├── apps/
│   │   ├── useraccount/  # 👤 User authentication & profiles
│   │   ├── property/  # 🏠 Property listings
│   │   ├── booking/  # 📅 Bookings & reservations
│   │   ├── chat/  # 💬 Chat system
│   ├── templates/
│   ├── static/
├── nginx/  # 🌐 Nginx configuration
├── .env.dev  # 🔐 Environment variables
├── .gitignore  # 🚫 Ignore files in Git
├── LICENSE  # 📜 License file
├── README.md  # 📖 Documentation
├── docker-compose.prod.yml  # 🐳 Production Docker setup
├── docker-compose.yml  # 🐳 Development Docker setup
```

## 🚀 Getting Started

To get started with this project, follow these steps:

### 🔧 Prerequisites

- **🐳 Docker**: Install Docker from [here](https://www.docker.com/get-started).

### 🛠 Installation

1. **📥 Clone the Repository**:

   ```bash
   git clone https://github.com/Epic-Codebase/Airbnb_clone_django_drf.git
   cd Airbnb_clone_django_drf
   ```

2. **📄 Set Up Environment Variables**:

   - Create a `.env.dev` file in the root directory.
   - Add necessary environment variables as required.

3. **🏗 Build and Run Docker Containers**:

   - For **development**:
     ```bash
     docker-compose up --build
     ```
   - For **production**:
     ```bash
     docker-compose -f docker-compose.prod.yml up --build
     ```

4. **🔄 Apply Migrations**:

   ```bash
   docker-compose exec web python manage.py migrate
   ```

5. **👤 Create a Superuser**:

   ```bash
   docker-compose exec web python manage.py createsuperuser
   ```

6. **📂 Collect Static Files**:

   ```bash
   docker-compose exec web python manage.py collectstatic --no-input --clear
   ```

Now, the application should be running at **`http://localhost:8000/`** 🚀

## 🔗 API Endpoints

### 👥 User Authentication

- `POST /api/auth/register/` → Register a user.
- `POST /api/auth/login/` → Login.
- `POST /api/auth/logout/` → Logout.

### 🏠 Property Management

- `GET /api/properties/` → List properties.
- `POST /api/properties/` → Create a property.
- `GET /api/properties/{id}/` → Get property details.
- `PUT /api/properties/{id}/` → Update property.
- `DELETE /api/properties/{id}/` → Delete property.

### 📅 Booking Management

- `GET /api/bookings/` → List bookings.
- `POST /api/bookings/` → Create booking.
- `GET /api/bookings/{id}/` → Get booking details.
- `PUT /api/bookings/{id}/` → Update booking.
- `DELETE /api/bookings/{id}/` → Cancel booking.

### 💬 Chat

- `GET /api/chat/` → Get chat messages.
- `POST /api/chat/` → Send a message.

## 🛠 Technologies Used

- **🐍 Django**: Python web framework.
- **⚡ DRF**: API toolkit for Django.
- **🐘 PostgreSQL**: Database.
- **🐳 Docker**: Containerization.
- **🌐 Nginx**: Reverse proxy.

## 🤝 Contributing

Contributions are welcome! ✨ Follow these steps:

1. **Fork** the repository.
2. **Create a new branch** (`git checkout -b feature/YourFeature`).
3. **Commit your changes** (`git commit -m 'Add YourFeature'`).
4. **Push to the branch** (`git push origin feature/YourFeature`).
5. **Open a Pull Request** 🚀.

## 📜 License

Licensed under **Apache-2.0**. See [LICENSE](https://github.com/Epic-Codebase/Airbnb_clone_django_drf/blob/main/LICENSE) 📃.

## 🎉 Acknowledgements

Big thanks to the **Django & DRF** communities for their amazing contributions! ❤️

