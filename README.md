A fork of selinux_MAF_fork; a test module designed to handle special kernels with the following layout: 

`/security/selinux/include/security.h`

```c
extern struct page *selinux_kernel_status_page(void);
```

`/security/selinux/ss/services.c`

```c
static void context_struct_compute_av(struct policydb *policydb,
                                      struct context *scontext,
                                      struct context *tcontext,
                                      u16 tclass,
                                      struct av_decision *avd,
                                      struct extended_perms *xperms);
```
Acknowledgments: [KernelPatch](https://github.com/bmax121/kernelpatch)