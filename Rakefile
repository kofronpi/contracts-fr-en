# encoding: UTF-8
require 'handlebars'
require 'json'

task default: [:handlebars, :pdf] do
end

task :handlebars do |t, args|
  handlebars = Handlebars::Context.new
  ['cp', 'cgv', 'pcc'].each do |file|
    File.write(
      "tmp/#{file}.md",
      handlebars.compile(
        File.read("src/#{ENV['PDF_LANGUAGE']}/#{file}.md")
      ).call(
        JSON.parse(
          File.read('config.json').force_encoding('UTF-8')
        )
      )
    )
  end
end

task :pdf do
  `mkdir contracts`
  ['cp', 'cgv', 'pcc'].each do |file|
    `rm contracts/#{file}.pdf`
    `gimli -f tmp/#{file}.md -o contracts`
  end
end