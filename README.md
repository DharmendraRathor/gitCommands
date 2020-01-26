<h1 style="color: #5e9ca0;">Important Git Commands&nbsp;</h1>
<table class="editorDemoTable">
	<thead>
		<tr>
			<td>Commands</td>
			<td>Description</td>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>git init</td>
			<td>
				<p class="p1">
					<span class="s1">Create git repository on locale machine.</span>
				</p>
			</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git Status</span>
				</p>
			</td>
			<td>
				<p class="p1">
					<span class="s1">View list of files modified.</span>
				</p>
			</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git clone username@host:/path/to/repository</span>
				</p>
			</td>
			<td>&nbsp;

				<p class="p1">
					<span class="s1">Checkout exiting git repository</span>
				</p>
			</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git checkout &lt;branchName&gt;</span>
				</p>
			</td>
			<td>Switch to existing branch</td>
		</tr>
		<tr>
			<td>
				<p class="p1">git checkout -b &lt;branchName&gt;</p>
			</td>
			<td>Create new branch and switch to that branch</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git add &lt;file name with path&gt;</span>
				</p>
			</td>
			<td>Add single file to staging</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git add *</span>
				</p>
			</td>
			<td>Add all file to staging</td>
		</tr>
		<tr>
			<td>  git stash list</td>
			<td>
				<p class="p1">
					<span class="s1">List of stash done earlier.</span>
				</p>
			</td>
		</tr>
		<tr></tr>
		<tr>
			<td>  git stash apply "stashId"  eg  git stash apply stash@{0}</td>
			<td>
				<p class="p1">
					<span class="s1">To apply stash .</span>
				</p>
			</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git commit -m "commit message "</span>
				</p>
			</td>
			<td>Commit files in staging // this is committed to local repository and not to remote</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git push</span>
				</p>
			</td>
			<td>Publish changes to remote repository</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git pull</span>
				</p>
			</td>
			<td>Pull changes from remote branch to your branch (this will fetch and merge changes)</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git branch&nbsp;</span>
				</p>
			</td>
			<td>List all branches on local respository and current active branch name as highlited</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git log 
						<br />git log -2
					</span>
				</p>
			</td>
			<td>View commit history</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git merge &lt;branchTobeMerged&gt;</span>
				</p>
			</td>
			<td>Merge branch with your local branch</td>
		</tr>
		<tr>
			<td>
				<p class="p1">
					<span class="s1">git diff</span>
				</p>
			</td>
			<td>View changes done before pushing it to remote.</td>
		</tr>
		<tr>
			<td>
				<p>&nbsp;git remote show &lt;branchName&gt;</p>
				<p>eg git remote show origin</p>
			</td>
			<td>View git remote url or remote branch details.&nbsp;</td>
		</tr>
		<tr>
			<td>git checkout -b &lt;branchName&gt; &lt;tagName&gt;</td>
			<td>&nbsp;Create branch from Tag in Github</td>
		</tr>
		<tr>
			<td>git cherry-pick &lt;commit-id&gt;
				<br />eg git cherry-pick ...31ff5e.....
			</td>
			<td>
				<p>&nbsp;Get Cherry picking commit</p>
				<p>if you have to cherry pick commit from one branch to another in Git repository with Commit id.</p>
			</td>
		</tr>
		<tr>
			<td>git branch newBranchName &lt;commit-id&gt;&nbsp;</td>
			<td>
				<p>Create new Git branch from Git commit</p>
				<p>Create new branch from git commit withouth checkingout new branch</p>
			</td>
		</tr>
		<tr>
			<td>git checkout -b newBranchName &lt;commit-id&gt;</td>
			<td>
				<p>Create new branch from git commit with checkingout new branch</p>
			</td>
		</tr>
		<tr>
			<td>&nbsp;

				<p>A Moving branches/tags from one git repository to another</p>
				<p>1. Clone existing git repo (source repository)
					<br />git clone --mirror &lt;source git url&gt;
				</p>
				<p>eg 
					<br />git clone --mirror git@github.com:source/source.git
				</p>
				<p>2. 
					<br />got to &lt;folder with name of repo&gt;
					<br />cd &lt;folder with name of repo&gt;
				</p>
				<p>3. Add remote repository ( destination repository )
					<br />git remote add new-origin &lt;destination git url&gt;
				</p>
				<p>eg 
					<br />git clone --mirror git@github.com:destination/destination.git
				</p>
				<p>4. Move all changes to destination repository
					<br />git push new-origin --mirror
				</p>
				<p>&nbsp;</p>
				<p>B If you only want to move some branches</p>
				<p>
					<br />1. git clone &lt;source git repository url&gt;
				</p>
				<p>2. checkout all branches to be moved to new git.
					<br /> git checkout &lt;branch&gt;
					<br />
					<br />3. verify branches to be moved using output of git branch command
					<br /> git branch 
					<br />
					<br />4. add destination repository 
					<br /> git remote add new-origin git@github.com:destination/destination.git
					<br />
					<br />5. move all local branches to destination repository
					<br /> git push --all new-origin 
					<br />
					<br />6. move all tags to destination repository
					<br /> git push --tags new-origin
				</p>
				<p>
					<br />C Move branch to new git repository and changing remote
				</p>
				<p>after doing steps mentioned above to move branch from one git to another , use following command to set new 
					<br />origin in git.
				</p>
				<p>git remote rm origin
					<br />git remote rename new-origin origin
				</p>
				<p>
					<br />
					<br />Note : 
					<br />If you have already moved some branches and want to move one more branch from source git.
					<br />Running following command might override destination branche or give error. 
					<br />It is always good to move all branches and tags to new repository and start using new repository.
				</p>
				<p>&nbsp;</p>
			</td>
			<td>
				<p>Moving branches/tags from one git repository to another</p>
			</td>
		</tr>
		<tr>
			<td>&nbsp;

				<p>You have branch having latest changes &ldquo;latestBranch&rdquo; and if you want to override master with latestBranch changes. 
					<br />Use following commands
				</p>
				<p>1. Checkout latestBranch.
					<br />git checkout latestBranch
				</p>
				<p>2. Merge latestBranch with master with strategy as ours. Current branch changes will be used in case of conflicts.
					<br />git merge -s ours master
				</p>
				<p>3. Checkout master branch.
					<br />git checkout master
				</p>
				<p>4. Merge master with latestBranch
					<br />git merge latestBranch
				</p>
				<p>5. Push master with latest code.
					<br />git push (git push origin master)
				</p>
				<p>you can also use git force push &ldquo;git push -f origin master&rdquo;. Please check branch history before running git push</p>
			</td>
			<td>
				<p>Replace/override Master branch with your latest branch in git</p>
			</td>
		</tr>
		<tr>
			<td>Revert merge request&nbsp;</td>
			<td>
				<p>Find commit id of merge request , it can also be seen from UI&nbsp;</p>
				<p>or using grep and git log command eg&nbsp;</p>
				<p>git log -200 | grep -B 20 "Merge pull request #12"</p>
				<p>&nbsp;</p>
				<p>Once you have commit id , run following command&nbsp;</p>
				<p>&nbsp;</p>
				<p>git revert -m 1 &lt;commitId&gt;</p>
				<p>&nbsp;</p>
				<p>In case of conflict resolve them manually and add files using "git add "</p>
				<p>&nbsp;</p>
				<p>(fix conflicts and run "git revert --continue")</p>
				<p>&nbsp;</p>
				<p>git push</p>
			</td>
		</tr>
		<tr>
			<td>Revert direct commit with commit Id&nbsp;</td>
			<td>
				<p>git rever &lt;commitID&gt;</p>
			</td>
		</tr>
		<tr>
			<td>Added file by mistake using "git add fileName.txt"  and want to remove it before commiting from index &nbsp;</td>
			<td>
				<p>git reset fileName.txt  </p>
			</td>
		</tr>
		<tr>
			<td>Revert "git add ." from index &nbsp;</td>
			<td>
				<p>git reset </p>
			</td>
		</tr>
		
		<tr>
			<td><br/> Set Git config username and email &nbsp;</td>
			<td>
				<p><br/>
				    git config --global user.name "firstName lastname" <br/>
git config --global user.email "abc@test.com" <br/>
 </p>
			</td>
		</tr>
		
		
		<tr>
			<td><br/><br/>Create new git repository&nbsp;</td>
			<td>
				<p><br/>
git clone  git@git.com:platform/project.git <br/>
cd "projectFolder"<br/>
touch README.md<br/>
git add README.md<br/>
git commit -m "add README"<br/>
git push -u origin master<br/><br/><br/> </p>
			</td>
		</tr>
	
		<tr>
			<td><br/><br/>Link existing code to Git repo &nbsp;</td>
			<td>
				<p>
cd existing_folder<br/>
git init<br/>
git remote add origin git@git.com:platform/project.git<br/>
git add .<br/>
git commit -m "Initial commit"<br/>
git push -u origin master<br/><br/>
</p>
			</td>
		</tr>
		
			<tr>
			<td><br/><br/>Link existing git repo to new git repo &nbsp;</td>
			<td>
				<p> cd existing_repo<br/>
git remote rename origin old-origin<br/>
git remote add origin git@git.com:platform/project.git<br/>
git push -u origin --all<br/>
git push -u origin --tags<br/> </p>
			</td>
		</tr>
		
	</tbody>
</table>
<p>
	<strong>&nbsp;</strong>
</p>
