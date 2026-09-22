FROM nixos/nix:latest

RUN printf 'experimental-features = nix-command flakes\nsandbox = false\n' >> /etc/nix/nix.conf

RUN nix profile add 'nixpkgs#pi-coding-agent'

RUN nix-collect-garbage -d

RUN rm -rf /root/.cache/nix

VOLUME ["/root/.pi/agent"]

ENTRYPOINT ["pi"]
