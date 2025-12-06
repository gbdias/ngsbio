FROM community.wave.seqera.io/library/fastqc_git:cf2183b876489165

ARG USERNAME=devpod
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
    # Create the DevPod agent directory and ensure the 'devpod' user owns it
    && mkdir -p /home/$USERNAME/.devpod \
    && chown -R $USERNAME:$USERNAME /home/$USERNAME

USER $USERNAME
