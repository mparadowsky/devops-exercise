FROM yndconsult/docker-ruby:2.6.3-centos7

WORKDIR "/app"

COPY . .

RUN yum install postgresql-devel -y
RUN curl -sL https://rpm.nodesource.com/setup_10.x | bash -
RUN yum install nodejs -y
RUN curl -sL https://dl.yarnpkg.com/rpm/yarn.repo | tee /etc/yum.repos.d/yarn.repo
RUN yum install yarn -y
RUN yarn upgrade @rails/webpacker

CMD /app/docker-entrypoint.sh