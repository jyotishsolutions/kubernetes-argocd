<h1>Command</h1>


<strong> >kubectl port-forward svc/argocd-server -n argocd 8080:443 </strong>

<h2>Login into argocd</h2>
<strong> >argocd login http://localhost:8080 </strong>

time="2025-04-25T17:50:59+01:00" level=fatal msg="dial tcp: address http://localhost:8080: too many colons in address"

<strong> >argocd login localhost:8080 </strong>

WARNING: server certificate had error: tls: failed to verify certificate: x509: certificate signed by unknown authority. Proceed insecurely (y/n)? y
Username: admin
Password:
'admin:login' logged in successfully
Context 'localhost:8080' updated

<strong> >argocd login localhost:8080 </strong>

<h2>creating application</h2>
<strong>>argocd app create app-1 --repo https://github.com/jyotishsolutions/kubernetes-argocd.git --path guestbook --dest-server https://kubernetes.default.svc --dest-namespace default </strong>


