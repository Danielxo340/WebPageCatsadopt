# Cat Adoption Website - Railway Deployment

## Deployment Steps for Railway:

### 1. Connect Repository
- In Railway dashboard, click "Deploy from GitHub repo"
- Select this repository
- Railway will automatically detect it's a Node.js project

### 2. Configure Environment Variables
Add these variables in Railway settings:
- `DATABASE_URL` - Your PostgreSQL connection string
- `NODE_ENV` - Set to "production"
- `PORT` - Railway sets this automatically

### 3. Database Setup
- Add PostgreSQL service in Railway
- Copy the DATABASE_URL from Railway PostgreSQL service
- Run database migration: `npm run db:push`

### 4. Build Configuration
Railway will automatically:
- Install dependencies with `npm install`
- Build the project
- Start the server with `npm run dev`

### 5. Custom Domain (Optional)
- Go to Settings > Domains
- Add your custom domain
- Configure DNS records as shown

## Project Structure:
- Frontend: React with Vite (client/)
- Backend: Express server (server/)
- Database: PostgreSQL with Drizzle ORM
- Build output: Combined in dist/

## Environment Requirements:
- Node.js 18+
- PostgreSQL database
- All dependencies listed in package.json