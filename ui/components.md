---
title: Components
description: Get familiar with the default user interface elements (widgets) in NativeScript.
position: 20
slug: components
previous_url: /ui-views,/ui/ui-views
---

# User Interface Widgets

NativeScript ships with a set of user interface [`views`](http://docs.nativescript.org/api-reference/modules/_ui_core_view_.html) (also known as widgets) which you can use to build the user interface of a mobile application. Most of these views wrap the corresponding native view for each platform while providing a common API for working with it. For example, the `Button` view renders an [`android.widget.Button`](http://developer.android.com/reference/android/widget/Button.html) on Android and [`UIButton`](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIButton_Class/) on iOS.

<ul class="component-list">
  <li><a href="#button">Button</a></li>
  <li><a href="#label">Label</a></li>
  <li><a href="#textfield">TextField</a></li>
  <li><a href="#textview">TextView</a></li>
  <li><a href="#searchbar">SearchBar</a></li>
  <li><a href="#switch">Switch</a></li>
  <li><a href="#slider">Slider</a></li>
  <li><a href="#progress">Progress</a></li>
  <li><a href="#activityindicator">ActivityIndicator</a></li>
  <li><a href="#image">Image</a></li>
  <li><a href="#listview">ListView</a></li>
  <li><a href="#htmlview">HtmlView</a></li>
  <li><a href="#webview">WebView</a></li>
  <li><a href="#tabview">TabView</a></li>
  <li><a href="#segmentedbar">SegmentedBar</a></li>
  <li><a href="#datepicker">DatePicker</a></li>
  <li><a href="#timepicker">TimePicker</a></li>
  <li><a href="#listpicker">ListPicker</a></li>
  <li><a href="#dialogs">Dialogs</a></li>
</ul>

<aside class="app-preview">
  <div class="app-type">
    <a data-type="ios" class="active">iOS</a>
    <a data-type="android">Android</a>
  </div>
  <div class="app-embed">
    <iframe src="https://appetize.io/embed/hcb273p7nr9fg7dnd1gd1cr15r?device=iphone5s&scale=100&orientation=portrait&osVersion=9.3&autoplay=true&xdocMsg=true" width="360px" height="587px" frameborder="0" scrolling="no"></iframe>
  </div>
</aside>

Defining the layout of the application is also an important part of the application development. For more information about the different layout containers that are available in NativeScript, see [The NativeScript Layout System]({%slug layouts %}).

> **TIP:** You can access the underlying native widget for each view at runtime using the following properties:
>
> * Android: `<view>.android`
> * iOS: `<view>.ios`
>
> Accessing the native widgets might be useful when you want to use some platform-specific functionalities of the widget. You can find information about the underlying native component for each view below.

## Button

The [Button]({%ns_cookbook ui/button%}) widget provides a standard button widget that reacts to a `tap` event.

``` XML
<Button class="btn btn-primary" text="Tap"></Button>
```

**Native Component**

| Android               | iOS      |
|:----------------------|:---------|
| [android.widget.Button](http://developer.android.com/reference/android/widget/Button.html) | [UIButton](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIButton_Class/) |

## Label

The [Label]({%ns_cookbook ui/label%}) widget provides a text label that shows read-only text.

``` XML
<Label text="The quick brown fox jumps over the lazy dog." class="h2" textWrap="true" />
```

**Native Component**

| Android               | iOS      |
|:----------------------|:---------|
| [android.widget.TextView](http://developer.android.com/reference/android/widget/TextView.html) | [UILabel](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UILabel_Class/) |

## TextField

The [TextField]({%ns_cookbook ui/text-field%}) widget provides an editable **single-line** text field.

``` XML
<StackLayout class="input-field">
  <TextField hint="Enter text..." class="input" />
  <StackLayout class="hr-light"></StackLayout>
</StackLayout>
```

**Native Component**

| Android               | iOS      |
|:----------------------|:---------|
| [android.widget.EditText](http://developer.android.com/reference/android/widget/EditText.html) | [UITextField](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextField_Class/) |

## TextView

The [TextView]({%ns_cookbook ui/text-view%}) widget provides an editable **multi-line** text view. 

You can use it to show multi-line text and implement text editing.

``` XML
<StackLayout class="input-field">
  <TextView hint="Edit text..." text="The quick brown fox jumps over the dog." class="input" />
</StackLayout>
```

**Native Component**

| Android               | iOS      |
|:----------------------|:---------|
| [android.widget.EditText](http://developer.android.com/reference/android/widget/EditText.html) | [UITextView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextView_Class/) |

## SearchBar

The [SearchBar]({%ns_cookbook ui/search-bar%}) widget provides a user interface for entering search queries and submitting requests to the search provider.

``` XML
<SearchBar id="searchBar" hint="Search" text="" />
```

**Native Component**

| Android               | iOS      |
|:----------------------|:---------|
| [android.widget.SearchView](http://developer.android.com/reference/android/widget/SearchView.html) | [UISearchBar](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchBar_Class/) |

## Switch

The [Switch]({%ns_cookbook ui/switch%}) widget provides a two-state toggle switch from which you can choose between two options.

``` XML
<Switch checked="true" class="switch" id="checked"/>
```

**Native Component**

| Android               | iOS      |
|:----------------------|:---------|
| [android.widget.Switch](http://developer.android.com/reference/android/widget/Switch.html) | [UISwitch](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISwitch_Class/) |

## Slider

The [Slider]({%ns_cookbook ui/slider%}) widget provides a slider that you can use to pick a numeric value within a configurable range.

``` XML
<Slider minValue="1" maxValue="100" value="50" class="slider" />
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.SeekBar](http://developer.android.com/reference/android/widget/SeekBar.html) | [UISlider](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISlider_Class/) |

## Progress

The [Progress]({%ns_cookbook ui/progress%}) widget is a visual bar indicator of a progress in a operation. It shows a bar representing the current progress of the operation.

``` XML
<Progress id="progress" row="0" value="50" maxValue="100" class="progress" />
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.ProgressBar](http://developer.android.com/reference/android/widget/ProgressBar.html) (indeterminate = false) | [UIProgressView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIProgressView_Class/) |

## ActivityIndicator

The [ActivityIndicator]({%ns_cookbook ui/activity-indicator%}) widget is a visual spinner indicator which shows that a task is in progress.

``` XML
<ActivityIndicator busy="true" class="activity-indicator" />
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.ProgressBar](http://developer.android.com/reference/android/widget/ProgressBar.html) (indeterminate = true) | [UIActivityIndicatorView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityIndicatorView_Class/) |

## Image

The [Image]({%ns_cookbook ui/image%}) widget shows an image. You can load the image from an [`ImageSource`](http://docs.nativescript.org/api-reference/modules/_image_source_.html) or from a URL.

``` XML
<Image src="~/img/nativescript.png" stretch="fill" />
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.ImageView](http://developer.android.com/reference/android/widget/ImageView.html) | [UIImageView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIImageView_Class/) |

## ListView

The [ListView]({%ns_cookbook ui/list-view%}) shows items in a vertically scrolling list. You can set an [`itemTemplate`](http://docs.nativescript.org/api-reference/modules/_ui_list_view_.knowntemplates.html) to specify how each item in the list should be displayed.

``` XML
<ListView items="{{ sampleItems }}" class="list-group">
    <ListView.itemTemplate>
        <StackLayout>
            <Label class="list-group-item" text="{{ title }}"/>  
        </StackLayout>
    </ListView.itemTemplate>
</ListView>
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.ListView](http://developer.android.com/reference/android/widget/ListView.html) | [UITableView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableView_Class/) |

## HtmlView

The [HtmlView]({%ns_cookbook ui/html-view%}) represents a view with HTML content. Use this component instead of WebView when you want to show just static HTML content.

``` XML
<HtmlView html="{{ htmlString }}" class="w-full h-full" />
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.TextView](http://developer.android.com/reference/android/widget/TextView.html) | [UILabel](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UILabel_Class/) |

## WebView

The [WebView]({%ns_cookbook ui/web-view%}) shows web pages. You can load a page from a URL or by navigating back and forward.

``` XML
<WebView src="https://nativescript.org" class="w-full h-full" />
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.webkit.WebView](http://developer.android.com/reference/android/webkit/WebView.html) | [UIWebView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIWebView_Class/) |

## TabView

With the [TabView]({%ns_cookbook ui/tab-view%}) control, you can implement tab navigation.

``` XML
<TabView id="tabViewContainer" class="tab-view">
    <TabView.items>
        <TabViewItem title="Tab 1" class="tab-view-item">
            <TabViewItem.view>
                <StackLayout class="page p-20">
                  <Label text="Tab 1 Content" class="h1" />
                  <StackLayout>
                      <Label text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas malesuada ipsum leo, eu semper nunc ultrices sed. Cras at feugiat ligula. Vivamus sagittis porttitor eros vel commodo. Etiam vitae suscipit justo, et volutpat magna. Etiam in neque sagittis, pretium ipsum ut, aliquam sapien. Mauris eget suscipit ex. Nam posuere purus at risus tincidunt viverra. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nunc ac dolor et sapien dapibus semper et in metus. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Pellentesque egestas dui sed ante interdum, at vulputate erat vulputate." textWrap="true" class="body" />
                  </StackLayout>
                </StackLayout>
            </TabViewItem.view>
        </TabViewItem>
        <TabViewItem title="Tab 2" class="tab-view-item">
            <TabViewItem.view>
                <StackLayout class="page p-20">
                  <Label text="Tab 2 Content" class="h1" />
                  <StackLayout>
                      <Label text="Nullam egestas in mauris et condimentum. Maecenas scelerisque porta nisl ut pharetra. Etiam ac urna et justo pulvinar congue ut et risus. Sed odio tortor, gravida sed massa sit amet, euismod elementum nisi. Sed suscipit nibh non eros gravida, sed scelerisque justo sollicitudin. Mauris turpis eros, hendrerit in sapien ut, eleifend malesuada risus. Quisque vestibulum porta rhoncus. Donec ullamcorper sem a auctor varius. Etiam elementum quam sit amet rutrum volutpat. In hac habitasse platea dictumst. Vestibulum nibh diam, laoreet eget velit eget, iaculis eleifend purus. Duis a ornare nibh, a mollis urna. Suspendisse potenti. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Sed lobortis et risus vel rutrum. Sed vel sem nunc." textWrap="true" class="body" />
                  </StackLayout>
                </StackLayout>
            </TabViewItem.view>
        </TabViewItem>
    </TabView.items>
</TabView>
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.support.v4.view.ViewPager](http://developer.android.com/reference/android/support/v4/view/ViewPager.html) | [UITabBarController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBarController_Class/) |

## SegmentedBar

With the [SegmentedBar]({%ns_cookbook ui/segmented-bar%}) control, you can implement discrete selection.

```XML
<SegmentedBar class="segmented-bar">
    <SegmentedBar.items>
        <SegmentedBarItem title="First" />
        <SegmentedBarItem title="Second" />
        <SegmentedBarItem title="Third" />
        
    </SegmentedBar.items>
</SegmentedBar>
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.TabHost](http://developer.android.com/reference/android/widget/TabHost.html) | [UISegmentedControl](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UISegmentedControl_Class/index.html) |

## DatePicker

With the [DatePicker]({%ns_cookbook ui/date-picker%}) control, you can pick a date.

```XML
<DatePicker day="{{day}}" month="{{month}}" year="{{year}}"></DatePicker>
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.DatePicker](http://developer.android.com/reference/android/widget/DatePicker.html) | [UIDatePicker](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDatePicker_Class/index.html) |

## TimePicker

With the [TimePicker]({%ns_cookbook ui/time-picker%}) widget, you can pick a time.

```XML
<TimePicker hour="{{hour}}" minute="{{min}}"></TimePicker>
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.TimePicker](http://developer.android.com/reference/android/widget/TimePicker.html) | [UIDatePicker](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDatePicker_Class/index.html) |

## ListPicker

With the [ListPicker]({%ns_cookbook ui/list-picker%}) widget, you can pick a value from a list.

```XML
<ListPicker items="{{sampleItems}}"></ListPicker>
```

**Native Component**

| Android                | iOS      |
|:-----------------------|:---------|
| [android.widget.NumberPicker](http://developer.android.com/reference/android/widget/NumberPicker.html) | [UIPickerView](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIPickerView_Class/index.html) |

## Dialogs

The [dialogs module]({%slug dialogs %}) lets you create and show dialog windows.

```TypeScript
import * as dialogs from 'ui/dialogs';

class ViewModel {
  public alert() {
    dialogs.alert('NativeScript is fun!');
  }

  public confirm() {
    dialogs.confirm('Are you sure?');
  }
  
  public prompt() {
    dialogs.prompt('Please enter your name:');
  }

  public login() {
    dialogs.login('Login');
  }
}
```

![dialog-confirm android](../img/gallery/android/dialogsPage_confirm.png "dialog-confirm android")![dialog-confirm ios](../img/gallery/ios/dialogsPage_confirm.png "dialog-confirm ios")
