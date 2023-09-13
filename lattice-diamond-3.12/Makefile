.PHONY: lattice-diamond-3.12

all: lattice-diamond-3.12

lattice-diamond-3.12:
	podman build ./ -t lattice-diamond-3.12
	toolbox create -i lattice-diamond-3.12

clean:
	-podman stop lattice-diamond-3.12
	-podman rm lattice-diamond-3.12
	-podman image rm lattice-diamond-3.12
	-toolbox rm lattice-diamond-3.12
