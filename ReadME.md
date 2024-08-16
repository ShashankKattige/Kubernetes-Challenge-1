
## Deploy the given architecture diagram for implementing a Jekyll SSG.


Click on each icon (including arrows) to see more details. Once done click on the Check button to test your work.



### 1.Build user information for martin in the default kubeconfig file: User = martin , client-key = /root/martin.key and client-certificate = /root/martin.crt (Ensure don't embed within the kubeconfig file)

### 2. Create a new context called 'developer' in the default kubeconfig file with 'user = martin' and 'cluster = kubernetes'

### 3. 'developer-role', should have all(*) permissions for services in development namespace

### 4. 'developer-role', should have all permissions(*) for persistentvolumeclaims in development namespace

### 5. 'developer-role', should have all(*) permissions for pods in development namespace

### 6. create rolebinding = developer-rolebinding, role= 'developer-role', namespace = development

### 7. rolebinding = developer-rolebinding associated with user = 'martin'

### 8. set context 'developer' with user = 'martin' and cluster = 'kubernetes' as the current context.

### 9. Service 'jekyll' uses targetPort: '4000', namespace: 'development'

### 10. Service 'jekyll' uses Port: '8080', namespace: 'development'

### 11. Service 'jekyll' uses NodePort: '30097', namespace: 'development'

### 12. pod: 'jekyll' has an initContainer, name: 'copy-jekyll-site', image: 'gcr.io/kodekloud/customimage/jekyll'

### 13. initContainer: 'copy-jekyll-site', command: [ "jekyll", "new", "/site" ] (command to run: jekyll new /site)

### 14. pod: 'jekyll', initContainer: 'copy-jekyll-site', mountPath = '/site'

### 15. pod: 'jekyll', initContainer: 'copy-jekyll-site', volume name = 'site'

### 16. pod: 'jekyll', container: 'jekyll', volume name = 'site'

### 17. pod: 'jekyll', container: 'jekyll', mountPath = '/site'

### 18. pod: 'jekyll', container: 'jekyll', image = 'gcr.io/kodekloud/customimage/jekyll-serve'

### 19. pod: 'jekyll', uses volume called 'site' with pvc = 'jekyll-site'

### 20. pod: 'jekyll' uses label 'run=jekyll'

### PVC:
### 21. Storage Request: 1Gi

  ###  Access modes: ReadWriteMany

  ###  pvc name = jekyll-site, namespace = development

   ### 'jekyll-site' PVC should be bound to the PersistentVolume called 'jekyll-site'.

   ![image](https://github.com/user-attachments/assets/5cd08454-edc8-4014-90af-865e95bdc970)
