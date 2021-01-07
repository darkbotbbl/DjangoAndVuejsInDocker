# develop stage
FROM node:lts-alpine as develop-stage

WORKDIR /app

# start app
CMD ["npm", "run", "serve"]

# install the dependencies
COPY package*.json ./

# when the building of the container is taking too long, 
# uncoment line 16 or from 14 to 16
# RUN rm ./package-lock.json
# RUN rm -r ./node_modules
# RUN npm cache clean --force

RUN npm install

# add /app/node_modules/.bin to $PATH
ENV PATH /app/node_modules/.bin:$PATH

RUN ls 

COPY . .