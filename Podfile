platform :ios, '15.0'

target 'LoopFollow' do
  use_frameworks!
  use_modular_headers!

  pod 'Charts', '~> 4.1'
  pod 'ShareClient', :git => 'https://github.com/loopandlearn/dexcom-share-client-swift.git', :branch => 'loopfollow'

  post_install do |installer|
    installer.pods_project.targets.each do |target|
      target.build_configurations.each do |config|
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0'
      end
    end
  end
end
