FROM mcr.microsoft.com/devcontainers/javascript-node

RUN apt-get update && \
    apt-get upgrade -y && \
    rm -rf /var/lib/apt/lists/* && \
    curl -s https://gist.githubusercontent.com/LukeChannings/09d53f5c364391042186518c8598b85e/raw/ac8cd8c675b985edd4b3e16df63ffef14d1f0e24/deno_install.sh | sh  && \
    export DENO_INSTALL=/root/.deno && \
    export PATH=$DENO_INSTALL/bin:$PATH && \
    echo "export DENO_INSTALL=/root/.deno" >> ~/.bashrc && \
    echo "export PATH=$DENO_INSTALL/bin:$PATH" >> ~/.bashrc && \
    echo '#!/bin/bash' >> /usr/bin/supabase && \
    echo 'npx supabase "$@"' >> /usr/bin/supabase && \
    chmod +x /usr/bin/supabase && \
    npx --yes supabase && \