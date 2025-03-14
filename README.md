<h1>Git &amp; GitHub Workflow Guide</h1>
<p>This guide explains the essential Git commands and workflows in simple, clear steps. Copy the commands directly into your terminal.</p>

<h2>Table of Contents</h2>
<ol>
  <li><a href="#setup"> Setup &amp; Repository Linking</a></li>
  <li><a href="#basic"> Basic Commands</a></li>
  <li><a href="#branches"> Branching &amp; Merging</a></li>
  <li><a href="#conflicts"> Handling Merge Conflicts</a></li>
  <li><a href="#practical"> Practical Workflow Example</a></li>
  <li><a href="#additional"> Additional Commands</a></li>
  <li><a href="#resources"> Learning Resources</a></li>
  <li><a href="#conclusion"> Conclusion &amp; Best Practices</a></li>
</ol>

<h2 id="setup">1. Setup &amp; Repository Linking</h2>
<h3>🔹 Using HTTPS</h3>
<pre><code>git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/your-username/my-project.git
git push -u origin main</code></pre>

<h3>🔹 Using SSH (Recommended)</h3>
<p>To use SSH instead of HTTPS, follow these steps:</p>
<pre><code>ssh-keygen -t rsa -b 4096 -C "your-email@example.com"  # Generate SSH key
eval "$(ssh-agent -s)"                                 # Start SSH agent
ssh-add ~/.ssh/id_rsa                                  # Add key to SSH agent
cat ~/.ssh/id_rsa.pub                                  # Copy & add to GitHub SSH settings
git remote add origin git@github.com:your-username/my-project.git
git push -u origin main</code></pre>

<h2 id="basic">2. Basic Commands</h2>
<ul>
  <li><code>git status</code> – Check modified, staged, or untracked files.</li>
  <li><code>git log</code> – View commit history.</li>
  <li><code>git diff</code> – See unstaged changes.</li>
  <li><code>git add [file]</code> – Stage a specific file.</li>
  <li><code>git commit -m "Your message"</code> – Commit staged changes.</li>
  <li><code>git pull origin main --allow-unrelated-histories</code> – Merge histories when pulling from another repo.</li>
</ul>

<h2 id="branches">3. Branching &amp; Merging</h2>
<h3>✅ Create, List, and Delete Branches</h3>
<pre><code>git branch <branch_name>       # Create a branch
git branch                     # List all local branches
git branch -a                  # List all branches (local & remote)
git branch -d <branch_name>     # Delete a branch (safe)
git checkout -b <branch_name>   # Create & switch to a new branch</code></pre>

<h3>✅ Merging & Rebasing</h3>
<pre><code>git merge <branch_name>         # Merge another branch
git merge --no-ff <branch_name> # Merge with a commit (no fast-forward)
git rebase <branch_name>        # Reapply commits on top of another branch</code></pre>

<h2 id="conflicts">4. Handling Merge Conflicts</h2>
<h3>✅ Identify & Resolve Conflicts</h3>
<pre><code>git status                      # Check conflicts
git diff                        # Show conflicting changes
git add <conflicted_file>       # Mark as resolved
git commit                      # Commit the resolution</code></pre>

<h3>✅ Stash Changes</h3>
<pre><code>git stash                       # Stash changes before merging
git stash pop                   # Apply stashed changes after merging</code></pre>

<h2 id="practical">5. Practical Workflow Example</h2>
<pre><code>git clone git@github.com:your-username/my-project.git  # Clone using SSH
git add filename.ext
git commit -m "Update file"
git push
git log
git pull origin main --allow-unrelated-histories  # Include if pulling from a different repo
git show <commit-hash></code></pre>

<h2 id="additional">6. Additional Commands</h2>
<ul>
  <li><code>git commit -m "message" --amend</code> – Modify last commit.</li>
  <li><code>git log --all --graph</code> – View commits visually.</li>
  <li><code>git remote -v</code> – List remote repositories.</li>
</ul>

<h2 id="resources">7. Learning Resources</h2>
<ul>
  <li><a href="https://www.youtube.com/playlist?list=PLeo1K3hjS3usJuxZZUBdjAcilgfQHkRzW" target="_blank">Git &amp; GitHub Tutorials (Codebasics)</a></li>
  <li><a href="https://youtu.be/apGV9Kg7ics?si=o6KoFjJ1-B8O1omi" target="_blank">Learn Git in Depth (Kunal Kushwaha)</a></li>
  <li><a href="https://www.coursera.org/learn/introduction-to-version-control" target="_blank">Version Control Course (Meta)</a></li>
</ul>

<h2 id="conclusion">8. Conclusion &amp; Best Practices</h2>
<ul>
  <li>Use SSH for secure authentication.</li>
  <li>Write clear commit messages.</li>
  <li>Use branches for features & fixes.</li>
  <li>Regularly pull updates.</li>
  <li>Review pull requests carefully before merging.</li>
</ul>
<p style="text-align: right;"> Muhammad Zafar Ul Haq</p>
