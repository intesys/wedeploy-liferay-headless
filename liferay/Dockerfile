FROM liferay/portal-snapshot:7.1.x-201812180852-d24b1d5

# Set maintainer of the docker image
# LABEL maintainer="Denis Signoretto <denis.signoretto@intesys.it>"

RUN mkdir -p /etc/liferay/mount/files

#
# Copy confiuguration file to container
#
COPY --chown=liferay:liferay configs/files/ /etc/liferay/mount/files/

#
# Copy scripts file, executed by entrypoint.sh before execution of catalina.sh run
#
COPY --chown=liferay:liferay configs/scripts/ /etc/liferay/mount/scripts/

#
#COPY --chown=liferay:liferay configs/deploy/ /etc/liferay/mount/deploy/
#

#RUN chown -R liferay:liferay /etc/liferay/mount