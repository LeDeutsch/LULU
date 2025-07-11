# 🚀 Déploiement d'un Site Statique avec Docker & Nginx

> **Auteur** : *Dinspel Ludwig*  
> **Projet DevOps - 2025 ESTIAM*


## 🎯 Objectif

Déployer un site statique HTML/CSS dans un conteneur Docker, accessible via Nginx, puis publier l’image sur Docker Hub.


## 🧩 Structure du projet

mon-site/
│
├── assets/
├── images/
├── elements.html
├── generic.html
├── index.html
├── LICENSE.txt
├── README.txt
└── Dockerfile


## 🐳 Dockerfile utilisé

dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80

docker-compose.yml:

version: "3.8"

services:
  web:
    build: ./mon-site
    container_name: lulu_web
    ports:
      - "8080:80"
    restart: unless-stopped


## 🚦 Commandes principales

docker-compose up --build

Accès au site : http://localhost:8080

## 📚 Explications

    Template utilisé : Massively par HTML5 UP

    Pourquoi Docker ?
    → Déploiement ultra-rapide, reproductible partout, versionnage du code et des images.

    Pourquoi Nginx ?
    → Serveur web très léger, parfait pour du statique, configuration ultra-minimale.


