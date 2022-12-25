# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: sayar <sayar@student.1337.ma>              +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/12/14 12:05:52 by sayar             #+#    #+#              #
#    Updated: 2022/12/24 08:28:37 by sayar            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

all : clean build

.PHONY : all build stop up clean fclean

build :
	mkdir -p /Users/sayar/data/wordpress
	mkdir -p /Users/sayar/data/mysql
	docker-compose -f srcs/docker-compose.yml up --build

stop :
	docker-compose -f srcs/docker-compose.yml down

up :
	docker-compose -f srcs/docker-compose.yml up

clean :
	rm -rf /Users/sayar/data/mysql
	rm -rf /Users/sayar/data/wordpress
	docker-compose -f srcs/docker-compose.yml down -v

fclean : clean
	docker system prune --force --all

