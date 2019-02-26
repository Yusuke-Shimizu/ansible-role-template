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
    # p "cp ./ansible-role-template/requirements.yml ./ansible-role-#{args.name}/"
    # p "cp ./ansible-role-template/inventory ./ansible-role-#{args.name}/"
    # p "cp ./ansible-role-template/main.yml ./ansible-role-#{args.name}/"

    sh "ansible-galaxy init ansible-role-#{args.name}"
    sh "cp ./ansible-role-template/requirements.yml ./ansible-role-#{args.name}/"
    sh "cp ./ansible-role-template/inventory ./ansible-role-#{args.name}/"
    sh "cp ./ansible-role-template/main.yml ./ansible-role-#{args.name}/"
    sh "cp ./ansible-role-template/Rakefile ./ansible-role-#{args.name}/"
    sh "cp ./ansible-role-template/ansible.cfg ./ansible-role-#{args.name}/"
    sh "cp -r ./ansible-role-template/spec ./ansible-role-#{args.name}/"
    sh "cp -r ./ansible-role-template/retry ./ansible-role-#{args.name}/"
    sh "cp -r ./ansible-role-template/log ./ansible-role-#{args.name}/"
  end
end
