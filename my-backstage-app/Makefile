local_build:
	yarn install --immutable
	yarn tsc
	yarn build:backend

docker_image_build: local_build
	docker image build . -f packages/backend/Dockerfile -t backstage-idp:v1.0

local_docker_run: docker_image_build
	docker run --env-file .env -it -p 7007:7007 backstage-idp:v1.0

local_start_up: docker_image_build
	docker-compose -f docker-compose.yaml up
