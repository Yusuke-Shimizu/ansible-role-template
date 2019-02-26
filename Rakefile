require 'rake'

task :ansible    => 'ansible:all'
task :default => :ansible

namespace :ansible do
  desc "Run Ansible"
  task :create, ['name'] do |task, args|
    p task
    p args
    p "ansible-role-#{args.name}"
    # p "ansible-galaxy init ansible-role-#{args.name}"
    # p "cp ./template/requirements.yml ./ansible-role-#{args.name}/"
    # p "cp ./template/inventory ./ansible-role-#{args.name}/"
    # p "cp ./template/main.yml ./ansible-role-#{args.name}/"

    sh "ansible-galaxy init ansible-role-#{args.name}"
    sh "cp ./template/requirements.yml ./ansible-role-#{args.name}/"
    sh "cp ./template/inventory ./ansible-role-#{args.name}/"
    sh "cp ./template/main.yml ./ansible-role-#{args.name}/"
    sh "cp ./template/Rakefile ./ansible-role-#{args.name}/"
    sh "cp ./template/ansible.cfg ./ansible-role-#{args.name}/"
    sh "cp -r ./template/spec ./ansible-role-#{args.name}/"
    sh "cp -r ./template/retry ./ansible-role-#{args.name}/"
    sh "cp -r ./template/log ./ansible-role-#{args.name}/"
  end
end
