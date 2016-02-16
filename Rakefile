# encoding: UTF-8
require 'handlebars'
require 'json'

SUPPORTED_LOCALES = ['fr', 'en']

task default: [:handlebars, :pdf] do
end

task :handlebars do |t, args|
  ENV['locale'] ||= 'fr'
  fail "Locale is invalid. Please choose from: #{SUPPORTED_LOCALES}"  \
    unless SUPPORTED_LOCALES.include? ENV['locale']
  handlebars = Handlebars::Context.new
  ['cp', 'cgv', 'pcc'].each do |file|
    File.write(
      "tmp/#{file}.md",
      handlebars.compile(
        File.read("src/#{ENV['locale']}/#{file}.md")
      ).call(
        JSON.parse(
          File.read('config.json').force_encoding('UTF-8')
        )
      )
    )
  end
end

task :pdf do
  `mkdir -p contracts`
  ['cp', 'cgv', 'pcc'].each do |file|
    `rm -f contracts/#{file}.pdf`
    `gimli -stylesheet style.css -f tmp/#{file}.md -o contracts`
  end
end
