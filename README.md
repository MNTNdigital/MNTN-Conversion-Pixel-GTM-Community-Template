### 🛠️ Google Tag Manager Community Templates (for Developers)

**Google Tag Manager (GTM) Community Templates** allow developers to build reusable, customizable tag, trigger, and variable templates for use within GTM. These templates help simplify third-party integrations and enforce clean, consistent tagging implementations — all without requiring end-users to write code.

Once published, your templates can be submitted to the [Community Template Gallery](https://tagmanager.google.com/gallery/), making them publicly accessible to GTM users worldwide.

---

### 🔄 How to Update Your Template

Follow these steps to update your GTM Community Template and keep the version history clean:

1. **Make Your Code Changes**

   - Modify your template code using the [GTM Template Editor](https://tagmanager.google.com/templates).
   - Once modified in GTM UI, you can export the template and then copy/paste its contents into `template.tpl` file.
   - Commit changes to your local Git repository.

2. **Test Locally**

   - Validate the template in GTM to ensure functionality, security, and performance.
   - Use the built-in template debugger and preview tools.

3. **Commit and Push Changes**

   ```bash
   git add .
   git commit -m "Describe your change here"
   git push origin main
   ```

4. **Get the Commit SHA**

   - Run `git log --oneline` or `git rev-parse HEAD` to get the latest commit SHA.
   - Use the **short SHA** (first 7 characters) for the metadata.

5. **Update `metadata.yaml`**
   Add a new version entry at the top of the `versions` section:

   ```yaml
   versions:
     - sha: abc1234
       changeNotes: |
         Added support for custom event parameters and improved error handling.
     - sha: previousSha
       changeNotes: Previous version notes
   ```

6. **Submit an Update to the Gallery**
   - Follow the [official update process](https://developers.google.com/tag-platform/tag-manager/templates/gallery#update_your_template).
   - Ensure your changes follow GTM’s [template policies and guidelines](https://developers.google.com/tag-platform/tag-manager/templates/policies).

---

### ✅ Best Practices

- Only list **published versions** in your `metadata.yaml`.
- Use **reverse chronological order** (newest first).
- Group incremental commits into a **single version entry** if they’re part of one release.

---

🔗 [Learn more about building GTM templates](https://developers.google.com/tag-platform/tag-manager/templates)

