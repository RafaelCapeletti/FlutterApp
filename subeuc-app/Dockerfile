FROM node:22-alpine
WORKDIR /app
COPY payload_*.txt /tmp/subeuc/
RUN cat /tmp/subeuc/payload_*.txt | base64 -d | tar -xz -C /app && rm -rf /tmp/subeuc
ENV NODE_ENV=production
EXPOSE 3000
CMD ["node", "server.js"]
