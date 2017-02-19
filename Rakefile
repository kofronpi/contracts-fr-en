# encoding: UTF-8
require 'handlebars'
require 'json'
require 'combine_pdf'

SUPPORTED_LOCALES = ['fr', 'en']
SUPPORTED_MODES = ['consulting', 'dev']

task default: [:handlebars, :pdf, :merge] do
end

task :handlebars do |t, args|
  ENV['locale'] ||= 'fr'
  ENV['mode'] ||= 'dev'
  raise "Locale is invalid. Please choose from: #{SUPPORTED_LOCALES}"  \
    unless SUPPORTED_LOCALES.include? ENV['locale']
  raise "Mode is invalid. Please choose from: #{SUPPORTED_MODES}"  \
    unless SUPPORTED_MODES.include? ENV['mode']
  handlebars = Handlebars::Context.new
  ['cp', 'cgv', 'pcc', 'maintenance'].each do |file|
    File.write(
      "tmp/#{file}.md",
      handlebars.compile(
        File.read("src/#{ENV['locale']}/#{ENV['mode']}/#{file}.md")
      ).call(
        JSON.parse(
          File.read('config.json').force_encoding('UTF-8')
        )
      )
    )
  end
end

task :pdf do
  `mkdir -p contracts/#{ENV['mode']}`
  ['cp', 'cgv', 'pcc', 'maintenance'].each do |file|
    `rm -f contracts/#{ENV['mode']}/#{file}.pdf`
    `gimli -stylesheet style.css -f tmp/#{file}.md -o contracts/#{ENV['mode']}`
  end
end

task :merge do
  pdf_name = ENV['locale'] == 'fr' ? 'contrat' : 'contract'
  (CombinePDF.load("contracts/#{ENV['mode']}/cp.pdf")  \
    << CombinePDF.load("contracts/#{ENV['mode']}/cgv.pdf")  \
    << CombinePDF.load("contracts/#{ENV['mode']}/pcc.pdf"))  \
    .save("contracts/#{ENV['mode']}/#{pdf_name}.pdf")
end
