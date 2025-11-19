# Team Fun AI - Frontend

A React application built with Rsbuild for the Team Fun AI project. This frontend allows admins to manage team members with funny personality traits, and members to chat with an AI that responds in their personalized style.

## 🚀 Tech Stack

- **Build Tool**: Rsbuild (Rust-based bundler)
- **Framework**: React 19
- **Language**: TypeScript
- **State Management**: Redux Toolkit
- **Routing**: React Router v7
- **Styling**: Tailwind CSS
- **HTTP Client**: Axios
- **Form Handling**: React Hook Form + Zod

## 📁 Project Structure

```
frontend/
├── src/
│   ├── features/           # Feature-based modules
│   │   ├── auth/          # Authentication
│   │   ├── chat/          # Chat interface
│   │   ├── users/         # User management
│   │   └── personalities/ # Personality traits
│   ├── lib/               # Core libraries
│   │   ├── api/           # API configuration
│   │   └── store/         # Redux store
│   ├── shared/            # Shared resources
│   │   ├── components/    # Reusable components
│   │   ├── hooks/         # Custom hooks
│   │   ├── types/         # TypeScript types
│   │   ├── utils/         # Utility functions
│   │   └── constants/     # Constants
│   ├── pages/             # Page components
│   ├── layouts/           # Layout components
│   ├── App.tsx            # Main app component
│   └── index.tsx          # Entry point
├── public/                # Static assets
├── rsbuild.config.ts      # Rsbuild configuration
├── tailwind.config.js     # Tailwind configuration
└── tsconfig.json          # TypeScript configuration
```

## 🎯 Features

### Implemented
- ✅ Authentication system (login/logout)
- ✅ JWT token management with auto-refresh
- ✅ Role-based access control (Admin/Member)
- ✅ Protected routes
- ✅ Chat interface with real-time messaging
- ✅ Redux state management
- ✅ Axios interceptors for API calls
- ✅ Responsive design with Tailwind CSS
- ✅ TypeScript for type safety

### To Be Connected (Backend Required)
- 🔄 User CRUD operations
- 🔄 Personality trait management
- 🔄 AI response integration
- 🔄 Chat history persistence

## 🛠️ Installation

1. Install dependencies:
```bash
pnpm install
```

2. Create environment file:
```bash
cp .env.example .env
```

3. Update `.env` with your API URL:
```env
VITE_API_URL=http://localhost:3001/api
```

## 🚀 Development

Start the development server:
```bash
pnpm dev
```

The app will be available at `http://localhost:3000`

## 🏗️ Build

Build for production:
```bash
pnpm build
```

Preview production build:
```bash
pnpm preview
```

## 📝 Available Scripts

- `pnpm dev` - Start development server
- `pnpm build` - Build for production
- `pnpm preview` - Preview production build

## 🔐 Authentication Flow

1. User enters credentials on login page
2. Frontend sends credentials to backend API
3. Backend validates and returns JWT tokens
4. Tokens stored in localStorage
5. Axios interceptor adds token to all requests
6. On 401 error, automatically refreshes token
7. On refresh failure, redirects to login

## 🎨 User Roles

### Admin
- Access to admin dashboard
- Manage team members
- Add/edit personality traits
- View all users

### Member
- Access to chat interface
- Send messages to AI
- Receive personalized responses
- View chat history





