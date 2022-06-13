# goals
1. minimal "extras" kubernetes multi-machine cluster that can run containerized applications.
	1. "raw" kubernetes or microk8s/k3s?
	2. docker or containerd or <something else>?
2. make these apps available through subdomains of `ignore.work` (reg'd on dreamhost).
3. ideally have no container "pinned" to a machine due to the persistent storage being on that machine.
	1. can this be done without something like [longhorn](https://longhorn.io/)?

# system
debian 11 or testing (w/ non-free firmware), headless/minimal
swap disabled (required for some kubernetes things)

# hardware
- node0
	- custom built desktop
	- Intel Core i5-4430 CPU @ 3.00GHz (haswell, 4 cores, 1 threads/core)
	- 16gb ram
	- Dell GT 730 OEM 2 GB (NVIDIA GeForce GT 730)
- node1-3
	- Dell Optiplex 3020
	- Intel Core i5-4590 CPU @ 3.30GHz (haswell, 4 cores, 1 threads/core)
	- 8gb ram
- tp-link 5 port 1 gigabit unmanaged switch, TL-SG1005D

# additional packages beyond base system
htop
micro
curl
sqlite3
blkid (longhorn)
open-iscsi (longhorn)