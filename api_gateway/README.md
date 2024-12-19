# ARCHITECTURE
We will serving this nginx as reverse proxy for our backend:
- Documents:
   + Generate ssl/tls: https://www.freecodecamp.org/news/how-to-get-https-working-on-your-local-development-environment-in-5-minutes-7af615770eec
- Requirements: 
   + Able to hide all microservice behind
   + Serving HTTPS
   + Authentications with jwt
- Testing:
   + HTTPS:
      - Have to create locally CA
      - Issued our Server cert signed by our CA
      - Add our CA to client side where we want to test
      - openssl genrsa -des3 -out rootCA.key 2048
      - openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 1024 -out rootCA.pem
   
   + Authentication:
      - Can able access public route not need to authenticate like register, login, ...
      - Need to validate token at gateway if not don't foward the package to microservices
