desc "Run the test suite"

task :test do
  Dir.chdir "TagListViewDemo" do 
    system "pod install"
  end

  build = "xcodebuild \
    -workspace TagListViewDemo/TagListViewDemo.xcworkspace \
    -scheme TagListViewDemo \
    -sdk iphonesimulator -destination 'platform=iOS Simulator,name=iPhone 6,OS=8.1'"
  system "#{build} test | xcpretty --test --color"  
end

task :default => :test

