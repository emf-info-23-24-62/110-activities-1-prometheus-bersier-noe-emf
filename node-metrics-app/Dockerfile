# Image Node.js légère basée sur Alpine Linux
FROM node:20-alpine             
# Répertoire de travail à l'intérieur du conteneur
WORKDIR /app                    
# Copie d'abord les fichiers de dépendances (optimise le cache Docker)
COPY package*.json ./           
# Installe uniquement les dépendances de production
RUN npm ci --omit=dev           
# Copie le reste du code source
COPY . .                        
# Documente le port utilisé (ne l'ouvre pas réellement)
EXPOSE 3000                     
# Commande lancée au démarrage du conteneur
CMD ["node", "index.js"]        
