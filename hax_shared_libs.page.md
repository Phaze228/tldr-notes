# Utilizing shared libraries for exploitation #
- Reference Knowledge Vault -- shared_libs.md

- Use ldd to find the shared libraries of an executable. Eg.
`ldd /bin/ls`

- Utilize LD_PRELOAD to execute code before a binary is activated.
` sudo LD_PRELOAD=/path/to/manipulated.so /bin/exe`


- Check RUNPATH configuration for binaries (typical in development)
`readelf -d <binary> `

- Verify function call via replacing .so with another .so to see what function is necessary.

- Setting PYTHONPATH before to change library imports
`sudo PYTHONPATH=/path/to/malicious/libs python_program`
