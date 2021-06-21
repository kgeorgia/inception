# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kgeorgia <kgeorgia@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/06/16 18:00:34 by kgeorgia          #+#    #+#              #
#    Updated: 2021/06/16 18:00:41 by kgeorgia         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

all:
	@docker-compose -f srcs/docker-compose.yml up

down:
	@docker-compose -f srcs/docker-compose.yml down

re:
	@docker-compose -f srcs/docker-compose.yml up --build
clean:
	@docker stop $$(docker ps -qa)
	@docker rm $$(docker ps -qa)
	@docker rmi -f $$(docker images -qa)
	@docker volume rm $$(docker volume ls -q)
	@docker network rm $$(docker network ls -q)
	rm -rf ~/data/db/*
	rm -rf ~/data/wp/*