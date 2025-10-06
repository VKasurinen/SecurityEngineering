2025-10-06T14:34:20+0000: Falco version: 0.41.3 (x86_64)
2025-10-06T14:34:20+0000: Falco initialized with configuration files:
2025-10-06T14:34:20+0000:    /etc/falco/config.d/falco.container_plugin.yaml | schema validation: ok
2025-10-06T14:34:20+0000:    /etc/falco/config.d/falco.iso8601_timeformat.yaml | schema validation: ok
2025-10-06T14:34:20+0000:    /etc/falco/falco.yaml | schema validation: ok
2025-10-06T14:34:20+0000: System info: Linux version 6.14.0-32-generic (buildd@lcy02-amd64-047) (x86_64-linux-gnu-gcc-13 (Ubuntu 13.3.0-6ubuntu2~24.04) 13.3.0, GNU ld (GNU Binutils for Ubuntu) 2.42) #32~24.04.1-Ubuntu SMP PREEMPT_DYNAMIC Tue Sep  2 14:21:04 UTC 2
2025-10-06T14:34:20+0000: Loading plugin 'container' from file /usr/share/falco/plugins/libcontainer.so
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'podman' container engine.
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/run/podman/podman.sock'
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'docker' container engine.
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/var/run/docker.sock'
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'cri' container engine.
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/run/containerd/containerd.sock'
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/run/crio/crio.sock'
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/run/k3s/containerd/containerd.sock'
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/run/host-containerd/containerd.sock'
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'containerd' container engine.
2025-10-06T14:34:20+0000: [libs]: container: * enabled container runtime socket at '/host/run/host-containerd/containerd.sock'
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'lxc' container engine.
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'libvirt_lxc' container engine.
2025-10-06T14:34:20+0000: [libs]: container: Enabled 'bpm' container engine.
2025-10-06T14:34:20+0000: Loading rules from:
2025-10-06T14:34:20+0000:    /etc/falco/falco_rules.yaml | schema validation: ok
2025-10-06T14:34:20+0000:    /etc/falco/falco_rules.local.yaml | schema validation: none
2025-10-06T14:34:20+0000: The chosen syscall buffer dimension is: 8388608 bytes (8 MBs)
2025-10-06T14:34:20+0000: Starting health webserver with threadiness 32, listening on 0.0.0.0:8765
2025-10-06T14:34:20+0000: Loaded event sources: syscall
2025-10-06T14:34:20+0000: Enabled event sources: syscall
2025-10-06T14:34:20+0000: Opening 'syscall' source with modern BPF probe.
2025-10-06T14:34:20+0000: One ring buffer every '2' CPUs.
2025-10-06T14:34:20+0000: [libs]: Trying to open the right engine!
2025-10-06T14:34:30.623982889+0000: Notice A shell was spawned in a container with an attached terminal | evt_type=execve user=root user_uid=0 user_loginuid=-1 process=sh proc_exepath=/usr/bin/dash parent=containerd-shim command=sh terminal=34816 exe_flags=EXE_WRITABLE|EXE_LOWER_LAYER container_id=d11ca4321185 container_name=hardcore_booth container_image_repository=ubuntu container_image_tag=latest k8s_pod_name=<NA> k8s_ns_name=<NA>
2025-10-06T14:34:45.235910465+0000: Critical Executing binary not part of base image | proc_exe=openssl proc_sname=dpkg gparent=ca-certificates proc_exe_ino_ctime=1759761282421632858 proc_exe_ino_mtime=3569093304029011968 proc_exe_ino_ctime_duration_proc_start=2814210097 proc_cwd=/etc/ssl/certs/ container_start_ts=1759761269712950519 evt_type=execve user=root user_uid=0 user_loginuid=-1 process=openssl proc_exepath=/usr/bin/openssl parent=update-ca-certi command=openssl rehash . terminal=34817 exe_flags=EXE_WRITABLE|EXE_UPPER_LAYER container_id=d11ca4321185 container_name=hardcore_booth container_image_repository=ubuntu container_image_tag=latest k8s_pod_name=<NA> k8s_ns_name=<NA>
^C2025-10-06T14:35:02+0000: SIGINT received, exiting...
Syscall event drop monitoring:
   - event drop detected: 0 occurrences
   - num times actions taken: 0
Events detected: 2
Rule counts by severity:
   CRITICAL: 1
   NOTICE: 1
Triggered rules by rule name:
   Terminal shell in container: 1
   Drop and execute new binary in container: 1
