Lessons

- Any internet server is susceptible to attack
- Threats are always changing
- There are best practices you can apply right now

The hacker wants to attack, mainly for three reasons
- Steal data
- Use the cluster to mine crypto
- Use the cluster to do DDOS attacks

Security practices
- Add security context to the container
```yaml
    securityContext:
        allowPrivilegesEscalation: false
        runAsNonRoot: true
        capabilities:
            drop:
             - ALL
        readOnlyRootFilesystem: true
```
- You can use Snyk to scan the Kubernetes files
Scan your infrastructure as code files including Kubernetes manifests
    - snik iac test <file.yml>

- Another practice is to update the Kubernetes version that you are using
Adding security patches

- Kubernetes Hardening Guide: NSA USA