FROM node as builder

ARG WORK_DIR=/home/node/om
WORKDIR ${WORK_DIR}

COPY package.json ${WORK_DIR}
COPY ./ ${WORK_DIR}

RUN yarn install
RUN yarn run buildDeploy


FROM node

ARG WORK_DIR=/home/node/om
WORKDIR ${WORK_DIR}

COPY --from=builder ${WORK_DIR}/package.json ${WORK_DIR}/package.json
COPY --from=builder ${WORK_DIR}/lite-server-config.json ${WORK_DIR}/lite-server-config.json
COPY --from=builder ${WORK_DIR}/deploy ${WORK_DIR}/deploy

RUN yarn install

ENTRYPOINT [ "yarn", "run", "startClient" ]
