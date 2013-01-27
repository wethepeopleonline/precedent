guard :bundler do
  watch("precedent.gemspec")
end

guard :rspec, :spec_paths => ['spec'], :cli => '-f progress' do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$}) { |m| "spec/lib/#{m[1]}_spec.rb" }
  watch(%r{^lib/(.+)\.treetop$}) { |m| "spec/lib/precedent/parser_spec.rb" }
  watch(%r{^lib/precedent/(nodes|node_patch)\.rb$}) { |m| "spec/lib/precedent/parser_spec.rb" }
end