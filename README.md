# Blood-Warrior-AI
 AI for Good hackathon focused on helping Thalassemia patients
# Clone and setup
git clone <repo-url>
cd thalassemia-care-platform

# Start backend
cd backend && python app.py

# Start frontend  
cd frontend && npm start

# Run ML training
cd ml-models && python train_model.py

# Setup Development Environment
git init thalassemia-care-platform
mkdir backend frontend ml-models database

# Backend Setup
cd backend
python -m venv venv
pip install flask sqlalchemy scikit-learn pandas numpy
flask db init

# Frontend Setup
cd ../frontend
npx create-react-app .
npm install axios recharts lucide-react tailwindcss

# Database Setup
docker run -d -p 5432:5432 --name thalassemia-db postgres:13
