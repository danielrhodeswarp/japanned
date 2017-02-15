#this image has a builtin nonroot 'node' user
FROM node:6.9

#ember server, live reload, test 'em scripts' (respectively)
EXPOSE 4200
EXPOSE 49152
EXPOSE 7357


VOLUME ["/ember_source"]

#actually, no, this prompts
#RUN adduser --disabled-password --ingroup users nonroot

# or just use image's 'node' user?
RUN useradd -g users nonroot

RUN npm -g update
RUN npm install -g ember-cli

#RUN cd mounted_in_container
#RUN ember new ember-project
#RUN cd ember-project
#RUN npm install

#CMD ["/bin/bash"]