# Ibadah & News Mobile App

## About The Project

This is a cross-platform mobile application for religious worship (ibadah) management and news distribution. The system allows users to access prayer schedules, religious articles, worship resources, and stay updated with the latest community news. Built with React Native and TypeScript for the frontend and Laravel for the backend API, this application delivers a seamless mobile experience across iOS and Android devices.

## Features

### Ibadah Module
- Prayer/Worship schedules and calendar
- Religious event management
- Scripture and religious readings
- Sermon archives and audio/video streaming
- Online donation system
- Community member directory
- Spiritual resource library
- Prayer reminders and notifications

### News Module
- Latest community news and announcements
- Event coverage and reporting
- Push notification for breaking news
- Content categorization and tagging
- Featured articles and highlights
- Media gallery (photos, videos)
- Comment and interaction system
- Offline reading mode

## Tech Stack

### Frontend (Mobile)
- React Native
- TypeScript (TSX)
- React Navigation
- Redux/Context API for state management
- Axios for API requests
- React Native Paper/UI Kitten for UI components
- React Native Vector Icons

### Backend (API)
- Laravel (PHP framework)
- MySQL/PostgreSQL database
- JWT Authentication
- RESTful API architecture
- File storage for media content

## Prerequisites

### For Frontend Development
- Node.js (v14.0.0 or higher)
- npm or yarn
- React Native CLI
- Android Studio (for Android development)
- Xcode (for iOS development, macOS only)
- JDK 11
- TypeScript

### For Backend Development
- PHP >= 8.1
- Composer
- MySQL/PostgreSQL
- Required PHP extensions (BCMath, Ctype, JSON, etc.)

## Installation

### Setting up the Backend (Laravel API)

1. Clone the repository
   ```bash
   git clone https://github.com/username/ibadah-news-app.git
   ```

2. Navigate to the backend directory
   ```bash
   cd ibadah-news-app/backend
   ```

3. Install PHP dependencies
   ```bash
   composer install
   ```

4. Create and configure .env file
   ```bash
   cp .env.example .env
   # Edit database and other configurations
   ```

5. Generate application key
   ```bash
   php artisan key:generate
   ```

6. Run migrations and seeders
   ```bash
   php artisan migrate --seed
   ```

7. Generate JWT secret
   ```bash
   php artisan jwt:secret
   ```

8. Start the development server
   ```bash
   php artisan serve
   ```

### Setting up the Frontend (React Native)

1. Navigate to the frontend directory
   ```bash
   cd ibadah-news-app/frontend
   ```

2. Install dependencies
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create and configure .env file for API endpoint
   ```bash
   cp .env.example .env
   # Edit API_URL and other configurations
   ```

4. Start Metro bundler
   ```bash
   npm start
   # or
   yarn start
   ```

5. Run on Android
   ```bash
   npm run android
   # or
   yarn android
   ```

6. Run on iOS (macOS only)
   ```bash
   npm run ios
   # or
   yarn ios
   ```

## Project Structure

### Frontend Structure
```
frontend/
├── src/
│   ├── assets/        # Images, fonts, etc.
│   ├── components/    # Reusable components
│   │   ├── ibadah/    # Ibadah module components
│   │   ├── news/      # News module components
│   │   └── shared/    # Common components
│   ├── navigation/    # React Navigation setup
│   ├── screens/       # Screen components
│   │   ├── ibadah/    # Ibadah screens
│   │   ├── news/      # News screens
│   │   └── auth/      # Authentication screens
│   ├── services/      # API services
│   ├── store/         # Redux/Context store
│   ├── types/         # TypeScript type definitions
│   ├── utils/         # Utility functions
│   └── App.tsx        # Root component
├── .env               # Environment variables
├── tsconfig.json      # TypeScript configuration
└── package.json       # Dependencies
```

### Backend Structure
```
backend/
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   │   ├── API/
│   │   │   │   ├── IbadahController.php
│   │   │   │   └── NewsController.php
│   │   ├── Middleware/
│   │   └── Resources/    # API Resources
│   ├── Models/
│   │   ├── Ibadah.php
│   │   ├── News.php
│   │   └── User.php
│   └── Services/
├── database/
│   ├── migrations/
│   └── seeders/
├── routes/
│   └── api.php
└── config/
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login and get JWT token
- `POST /api/auth/logout` - Logout and invalidate token
- `GET /api/auth/user` - Get authenticated user

### Ibadah Module
- `GET /api/ibadah/schedules` - Get prayer schedules
- `GET /api/ibadah/events` - Get worship events
- `GET /api/ibadah/resources` - Get spiritual resources
- `GET /api/ibadah/sermons` - Get sermon archives

### News Module
- `GET /api/news` - Get all news articles
- `GET /api/news/{id}` - Get specific news article
- `GET /api/news/categories` - Get news categories
- `POST /api/news/{id}/comments` - Add comment to news

## Building for Production

### Frontend
```bash
cd frontend
npm run build:android
# or
npm run build:ios
```

### Backend
1. Configure your production environment variables
2. Optimize Composer autoloader
   ```bash
   composer install --optimize-autoloader --no-dev
   ```
3. Set up proper web server configuration
4. Set up proper database backup strategies

## Additional Resources

- [React Native Documentation](https://reactnative.dev/docs/getting-started)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [Laravel Documentation](https://laravel.com/docs)
- [React Navigation Documentation](https://reactnavigation.org/docs/getting-started)

## Contributing

Please read the contribution guidelines before submitting pull requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [React Native Community](https://github.com/react-native-community)
- [Laravel Community](https://laravel.com/docs/contributions)
- [Open Source Initiatives](https://opensource.org/)
