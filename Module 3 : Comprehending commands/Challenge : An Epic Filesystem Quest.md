# An Epic Filesystem QUest
The challenge requires us to use our knowledge of cat, ls and cd commands and go on a long quest to find the flag which is hidden in a faraway file using the clues and hints dropped at several stages.
## My Solve
**Flag:** 'pwn.college{MHjwMk7F5KOoS2e6--CwU2fEFsf.QX5IDO0wSOxkjNzEzW}'
In this challenge we had to initially enter the '/' directory and use 'ls' command to find the initial clue contained in 'DOSSIER'. Similarly we had to navigate to the other directory mentioned in 'DOSSIER' to find a furthur clue. A few variations where we had to include '-a' flag along with 'ls' command to read through the hidden files and the one where we had to use the absolute path of a directory to access it instead of 'cd'ing into the encircling directory and simply using 'cat' were included.
```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
DOSSIER  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat DOSSIER
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/scipy/_lib/__pycache__

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/python3/dist-packages/scipy/_lib/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/_lib/__pycache__$ ls
BLUEPRINT                  _numpy_compat.cpython-38.pyc  _util.cpython-38.pyc      six.cpython-38.pyc
__init__.cpython-38.pyc    _testutils.cpython-38.pyc     _version.cpython-38.pyc
_ccallback.cpython-38.pyc  _threadsafety.cpython-38.pyc  decorator.cpython-38.pyc
_gcutils.cpython-38.pyc    _tmpdirs.cpython-38.pyc       doccer.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/_lib/__pycache__$ cat BLUEPRINT
Lucky listing!
The next clue is in: /usr/lib/python3/dist-packages/ipython_genutils/testing/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/_lib/__pycache__$ cd /usr/lib/python3/dist-packages/ipython_genutils/testing/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/ipython_genutils/testing/__pycache__$ ls -a
.  ..  .MESSAGE  __init__.cpython-38.pyc  decorators.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/ipython_genutils/testing/__pycache__$ cat .MESSAGE
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/include/uapi/scsi/fc

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/ipython_genutils/testing/__pycache__$ cd /opt/linux/linux-5.4/include/uapi/scsi/fc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/scsi/fc$ ls -a
.  ..  .SPOILER  fc_els.h  fc_fs.h  fc_gs.h  fc_ns.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/scsi/fc$ cat .SPOILER
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/alpha/kernel

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/scsi/fc$ cd /opt/linux/linux-5.4/arch/alpha/kernel
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/alpha/kernel$ ls
Makefile         core_marvel.c    err_impl.h    irq_pyxis.c     pci_iommu.c   srm_env.c        sys_nautilus.c  syscalls
README           core_mcpcia.c    err_marvel.c  irq_srm.c       perf_event.c  srmcons.c        sys_noritake.c  systbls.S
asm-offsets.c    core_polaris.c   err_titan.c   machvec_impl.h  process.c     sys_alcor.c      sys_rawhide.c   time.c
audit.c          core_t2.c        es1888.c      module.c        proto.h       sys_cabriolet.c  sys_ruffian.c   traps.c
binfmt_loader.c  core_titan.c     gct.c         osf_sys.c       ptrace.c      sys_dp264.c      sys_rx164.c     vmlinux.lds.S
bugs.c           core_tsunami.c   head.S        pc873xx.c       rtc.c         sys_eb64p.c      sys_sable.c
console.c        core_wildfire.c  io.c          pc873xx.h       setup.c       sys_eiger.c      sys_sio.c
core_apecs.c     entry.S          irq.c         pci-noop.c      signal.c      sys_jensen.c     sys_sx164.c
core_cia.c       err_common.c     irq_alpha.c   pci-sysfs.c     smc37c669.c   sys_marvel.c     sys_takara.c
core_irongate.c  err_ev6.c        irq_i8259.c   pci.c           smc37c93x.c   sys_miata.c      sys_titan.c
core_lca.c       err_ev7.c        irq_impl.h    pci_impl.h      smp.c         sys_mikasa.c     sys_wildfire.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/alpha/kernel$ cat README
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/alpha/kernel$ cd /usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls
HINT  config.js  jax.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ cat HINT
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__
TRACE-TRAPPED            connectivity.cpython-38.pyc  mixing.cpython-38.pyc           pairs.cpython-38.pyc
__init__.cpython-38.pyc  correlation.cpython-38.pyc   neighbor_degree.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
/usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
/usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls -a /usr/local/lib/python3.
8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
/usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
bash: /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED: Permission denied
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ cat  /usr/local/lib/python3.8/dist-packages/networkx/algorithms/assortativity/__pycache__/TRACE-TRAPPED
Lucky listing!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script
Regular  WHISPER-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script/Regular
Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ ls -a /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script/Regular
.  ..  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$  ls /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script/WHISPER-TRAPPED
/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script/WHISPER-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ cat /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Latin-Modern/Script/WHISPER-TRAPPED
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/sage/libs/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/PreviewHTML$ cd /usr/lib/python3/dist-packages/sage/libs/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/libs/__pycache__$ ls
INSIGHT  __init__.cpython-38.pyc  all.cpython-38.pyc  giac.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/libs/__pycache__$ cat INSIGHT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{MHjwMk7F5KOoS2e6--CwU2fEFsf.QX5IDO0wSOxkjNzEzW}
```

## What I Learned
I revised the concepts learnt so far containing cd, cat, ls, ls -a, absolute path mentioning etc. I also learnt how fun as well as challenging such quests can be if the basics are very clear.
## References
None.
