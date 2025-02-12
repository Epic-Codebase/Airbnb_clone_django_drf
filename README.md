# Airbnb Clone API Backend

Welcome to the Airbnb Clone API Backend, a robust and scalable backend solution for an Airbnb-like application, built using Django Rest Framework (DRF). This project provides a comprehensive set of features to manage properties, bookings, user authentication, and more.

## Features

- **User Authentication**: Secure user registration and login functionalities.
- **Property Categorization**: Classify properties into categories such as Beach, Villas, Cabins, and Tiny Homes.
- **Property Management**: Create, update, and manage property listings with specific categories.
- **Booking System**: Book properties for specified date ranges.
- **User Listings**: View properties hosted by a specific user.
- **Reservations Management**: Users can view their booked properties.
- **Host Profiles**: Detailed profiles for property hosts.
- **Property Search**: Search for properties based on location, check-in and check-out dates, and the number of guests.
- **Real-time Chat**: Communicate with property owners after booking through a chat system.

## Project Structure

```
Airbnb_clone_django_drf/
├── djangobnb_backend/
│   ├── djangobnb_backend/  # Django project settings and configurations
│   ├── apps/
│   │   ├── useraccount/  # Manages user authentication and profiles
│   │   ├── property/  # Handles property listings and categories
│   │   ├── booking/  # Manages property bookings and reservations
│   │   ├── chat/  # Implements the real-time chat feature
│   ├── templates/
│   ├── static/
├── nginx/  # Configuration files for Nginx
├── .env.dev  # Environment variables for development
├── docker-compose.prod.yml  # Docker Compose configuration for production
├── docker-compose.yml  # Docker Compose configuration for development
```

## Getting Started

To get a local copy of the project up and running, follow these steps.

### Prerequisites

- **Docker**: Ensure Docker is installed on your system. You can download it from [here](https://www.docker.com/get-started).

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Epic-Codebase/Airbnb_clone_django_drf.git
   cd Airbnb_clone_django_drf
   ```

2. **Set Up Environment Variables**:

   - Create a `.env.dev` file in the root directory.
   - Add the necessary environment variables as specified in the `.env.dev` file.

3. **Build and Run Docker Containers**:

   - For development:
     ```bash
     docker-compose up --build
     ```
   - For production:
     ```bash
     docker-compose -f docker-compose.prod.yml up --build
     ```

4. **Apply Migrations**:

   ```bash
   docker-compose exec web python manage.py migrate
   ```

5. **Create a Superuser**:

   ```bash
   docker-compose exec web python manage.py createsuperuser
   ```

6. **Collect Static Files**:

   ```bash
   docker-compose exec web python manage.py collectstatic --no-input --clear
   ```

The application should now be running and accessible at `http://localhost:8000/`.

## API Endpoints

The API provides the following endpoints:

- **User Authentication**:

  - `POST /api/auth/register/`: Register a new user.
  - `POST /api/auth/login/`: Log in a user.
  - `POST /api/auth/logout/`: Log out the current user.

- **Property Management**:

  - `GET /api/properties/`: List all properties.
  - `POST /api/properties/`: Create a new property.
  - `GET /api/properties/{id}/`: Retrieve a specific property.
  - `PUT /api/properties/{id}/`: Update a specific property.
  - `DELETE /api/properties/{id}/`: Delete a specific property.

- **Booking Management**:

  - `GET /api/bookings/`: List all bookings.
  - `POST /api/bookings/`: Create a new booking.
  - `GET /api/bookings/{id}/`: Retrieve a specific booking.
  - `PUT /api/bookings/{id}/`: Update a specific booking.
  - `DELETE /api/bookings/{id}/`: Cancel a specific booking.

- **Chat**:

  - `GET /api/chat/`: Retrieve chat messages.
  - `POST /api/chat/`: Send a new chat message.

For a detailed API documentation, please refer to the project's documentation or use tools like Postman to explore the endpoints.

## Technologies Used

- **Django**: High-level Python web framework.
- **Django Rest Framework (DRF)**: Powerful and flexible toolkit for building Web APIs.
- **PostgreSQL**: Relational database for storing application data.
- **Docker**: Containerization platform for deploying applications.
- **Nginx**: Web server used as a reverse proxy.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add YourFeature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

Please ensure your code adheres to the project's coding standards and includes appropriate test coverage.

## License

This project is licensed under the Apache-2.0 License. See the [LICENSE](https://github.com/Epic-Codebase/Airbnb_clone_django_drf/blob/main/LICENSE) file for more information.

## Acknowledgements

Special thanks to the Django and DRF communities for their invaluable resources and support.

