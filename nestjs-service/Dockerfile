# Используйте официальный образ Node.js как базовый
FROM node:20-alpine

# Установите рабочую директорию
WORKDIR /app

# Копируйте package.json и package-lock.json
COPY package*.json ./

# Установите зависимости
RUN npm install

# Копируйте исходный код в контейнер
COPY . .

# Постройте проект
RUN npm run build

# Установите точку входа
CMD ["npm", "run", "start:prod"]

# Откройте порт для внешнего доступа
EXPOSE 3000