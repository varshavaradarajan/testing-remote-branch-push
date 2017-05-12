task :bump do
  remote_name = 'origin'
  repo_url = `git config --get remote.#{remote_name}.url`.strip
  rm_rf "build"
  sh("git clone #{repo_url} build --branch foo-1 --depth 1 --quiet")
  cd "build" do
    sh("echo hello >> foo-1.txt; git add foo-1.txt; git commit -m 'go-user-on-foo-1'; git push ")
  end
end
