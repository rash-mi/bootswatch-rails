#!/usr/bin/env rake
require "bundler/gem_tasks"

#Added 'default' theme for bootswatch3, and, removed spruce and spacehero
THEMES = %w(
  amelia
  cerulean
  cosmo
  cyborg
  default
  flatly
  journal
  readable
  simplex
  slate
  spacelab
  united
).freeze

#Update src and dest to bootswatch3
LESS_FILES = FileList["bootswatch3/{#{THEMES.join(',')}}/*.less"]
SCSS_FILES = LESS_FILES.pathmap(
  'vendor/assets/stylesheets/bootswatch3/%-1d/_%n.scss'
)

SCSS_FILES.zip(LESS_FILES).each do |target, source|
  directory File.dirname(target)

  file target => [File.dirname(target), source] do
    sh "./converter #{source} #{target}"
  end
end

desc 'Imprecisely convert LESS files to SCSS files'
task convert: SCSS_FILES
