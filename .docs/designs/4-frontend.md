[<< Back](./../design.md)

# Frontend Design Specification

## Overview

This document captures the complete frontend application specification, design system, and architecture. It serves as the single source of truth for all UI/UX decisions and implementation details. This specification ensures the frontend is not just functional, but truly beautiful and modern.

**MANDATORY DEFAULTS**: All frontends must include responsive design supporting desktop and mobile devices, unless explicitly specified otherwise by the user.

## 📱 **MANDATORY RESPONSIVE DESIGN REQUIREMENTS**

**CRITICAL**: Every frontend application MUST support responsive design across desktop and mobile devices unless the user explicitly specifies otherwise.

### **Default Responsive Standards**:

**Required Device Support**:

- **Desktop**: 1024px+ (Primary development and business use)
- **Tablet**: 768px - 1023px (Intermediate layouts)
- **Mobile**: 375px - 767px (Essential mobile experience)

**Implementation Requirements**:

- **Mobile-First Development**: Build for mobile first, enhance for desktop
- **Flexible Grid Systems**: CSS Grid/Flexbox or Ant Design's responsive grid
- **Responsive Typography**: Scalable text sizes across all breakpoints
- **Touch Optimization**: 44px minimum touch targets for mobile
- **Navigation Adaptation**: Collapsible menus and mobile-friendly navigation

**Quality Assurance**:

- **Playwright Testing**: Mandatory screenshot tests at all breakpoints
- **Cross-Device Validation**: Test on actual mobile devices when possible
- **Performance Optimization**: Fast loading on mobile networks
- **Accessibility**: Keyboard navigation and screen reader compatibility

**When Responsive Design is NOT Required**:

- User explicitly requests desktop-only application
- Specialized hardware/kiosk applications
- Technical constraints preventing responsive implementation
- User specifies single-device targeting

## 🎨 **GAIA's UI/UX EXPERTISE** (When No Inspiration Provided)

### **Automatic Design Intelligence**

When users don't provide visual inspiration or UI/UX directives, GAIA automatically becomes the expert UI/UX designer, analyzing the target audience and crafting the perfect interface.

### **Audience-Driven Design Matrix**

#### **Business/Enterprise Applications**

**Characteristics**: Professional, trustworthy, efficient
**Color Palette**:

- Primary: Deep blues (#1E40AF, #3B82F6) or sophisticated grays (#374151, #6B7280)
- Accent: Professional greens (#059669, #10B981) or warm oranges (#EA580C, #F97316)
  **Typography**: Clean sans-serif (Inter, Roboto, Open Sans)
  **Layout**: Grid-based, data-dense, clear hierarchy
  **Examples**: Stripe, Linear, Notion, Salesforce Lightning

#### **Consumer/General Applications**

**Characteristics**: Friendly, approachable, intuitive
**Color Palette**:

- Primary: Warm blues (#2563EB, #3B82F6) or friendly purples (#7C3AED, #8B5CF6)
- Accent: Energetic colors (#EF4444, #F59E0B, #10B981)
  **Typography**: Rounded, friendly fonts (Inter, Poppins, Nunito)
  **Layout**: Card-based, whitespace-heavy, mobile-first
  **Examples**: Airbnb, Spotify, Instagram, Apple

#### **Creative/Portfolio Applications**

**Characteristics**: Bold, expressive, showcase-focused
**Color Palette**:

- Primary: Bold, artistic colors (#DC2626, #7C2D12, #1F2937)
- Accent: Vibrant, creative colors (#F59E0B, #8B5CF6, #EC4899)
  **Typography**: Distinctive fonts (Outfit, Playfair Display, custom)
  **Layout**: Asymmetrical, image-heavy, creative grids
  **Examples**: Behance, Dribbble, Awwwards, Adobe

#### **Technical/Developer Applications**

**Characteristics**: Functional, customizable, information-dense
**Color Palette**:

- Primary: Dark themes (#111827, #1F2937) with accent colors (#3B82F6, #10B981)
- Light: Clean grays (#F9FAFB, #F3F4F6) with technical blues
  **Typography**: Monospace options (JetBrains Mono, Fira Code) + sans-serif
  **Layout**: Dashboard-style, customizable panels, terminal-inspired
  **Examples**: GitHub, VS Code, Vercel, Figma

### **GAIA's Creative Process**

1. **Audience Analysis**: Extract target user type from project description
2. **Industry Research**: Apply industry-specific design patterns and expectations
3. **Color Psychology**: Select colors that evoke appropriate emotions and trust
4. **Information Architecture**: Design user flows that match user mental models
5. **Accessibility Integration**: Ensure inclusive design from the ground up
6. **Modern Trends Integration**: Apply current design trends appropriately

### **Default Design Decisions** (When Creating Original UI)

#### **Color Strategy**:

- **Primary Color**: Choose based on industry (blue for trust, green for growth, purple for creativity)
- **Accent Colors**: Complementary colors that enhance, not compete
- **Neutral Palette**: Modern grays with proper contrast ratios (4.5:1 minimum)
- **Semantic Colors**: Green for success, red for errors, amber for warnings, blue for info

#### **Typography Hierarchy**:

- **Display/Hero**: 3.5rem (56px) - Landing page headlines
- **H1**: 2.5rem (40px) - Page titles
- **H2**: 2rem (32px) - Section headers
- **H3**: 1.5rem (24px) - Subsection headers
- **Body Large**: 1.125rem (18px) - Important content
- **Body**: 1rem (16px) - Standard content
- **Small**: 0.875rem (14px) - Meta information
- **Caption**: 0.75rem (12px) - Fine print

#### **Spacing System** (8px base):

- **XS**: 4px - Icon spacing, small gaps
- **SM**: 8px - Element padding, tight spacing
- **MD**: 16px - Standard spacing between elements
- **LG**: 24px - Section spacing
- **XL**: 32px - Large section breaks
- **2XL**: 48px - Major layout divisions
- **3XL**: 64px - Hero section spacing

#### **Component Defaults**:

- **Buttons**: Rounded corners (8px), hover states, focus rings
- **Cards**: Subtle shadows, rounded corners (12px), proper padding
- **Forms**: Clear labels, proper spacing, validation states
- **Navigation**: Intuitive hierarchy, clear active states
- **Loading States**: Skeleton screens, progressive loading
- **Empty States**: Helpful illustrations, clear next steps

## 🎨 Visual Inspiration & Design Direction

### Design References

- **Primary Inspiration**: `[LINKS_TO_SPECIFIC_APPS/WEBSITES]`
- **Secondary References**: `[ADDITIONAL_INSPIRATION_SOURCES]`
- **Target Aesthetic**: `[MODERN_MINIMALIST/RICH_DETAILED/CREATIVE_BOLD/ENTERPRISE_PROFESSIONAL/ETC]`

### Design Philosophy

- **Core Principle**: `[BEAUTY_THROUGH_SIMPLICITY/SOPHISTICATED_DETAIL/BOLD_CREATIVITY/ETC]`
- **User Experience Goals**: `[INTUITIVE_NAVIGATION/DELIGHTFUL_INTERACTIONS/EFFICIENT_WORKFLOWS/ETC]`
- **Brand Personality**: `[TRUSTWORTHY/INNOVATIVE/PLAYFUL/PROFESSIONAL/ETC]`

## Design System

### Color Palette

**Primary Colors** (Based on inspiration/brand):

- Primary: `#[HEX_CODE]` - Main brand color for CTAs and primary actions
- Primary Light: `#[HEX_CODE]` - Hover states and backgrounds
- Primary Dark: `#[HEX_CODE]` - Active states and emphasis
- Secondary: `#[HEX_CODE]` - Accent color for highlights and secondary actions
- Tertiary: `#[HEX_CODE]` - Supporting color for variety and interest

**Neutral Palette** (Modern, sophisticated neutrals):

- White: `#FFFFFF` - Pure white for backgrounds
- Gray 50: `#[HEX_CODE]` - Lightest gray for subtle backgrounds
- Gray 100: `#[HEX_CODE]` - Very light gray for disabled states
- Gray 200: `#[HEX_CODE]` - Light gray for borders
- Gray 300: `#[HEX_CODE]` - Medium-light gray for secondary text
- Gray 400: `#[HEX_CODE]` - Medium gray for placeholders
- Gray 500: `#[HEX_CODE]` - True gray for secondary text
- Gray 600: `#[HEX_CODE]` - Dark gray for primary text
- Gray 700: `#[HEX_CODE]` - Very dark gray for headings
- Gray 800: `#[HEX_CODE]` - Almost black for emphasis
- Gray 900: `#[HEX_CODE]` - Pure black for maximum contrast

**Semantic Colors** (Modern, accessible):

- Success: `#10B981` - Green for success states
- Success Light: `#D1FAE5` - Light green for success backgrounds
- Warning: `#F59E0B` - Amber for warning states
- Warning Light: `#FEF3C7` - Light amber for warning backgrounds
- Error: `#EF4444` - Red for error states
- Error Light: `#FEE2E2` - Light red for error backgrounds
- Info: `#3B82F6` - Blue for informational states
- Info Light: `#DBEAFE` - Light blue for info backgrounds

## 🔔 **MANDATORY NOTIFICATION SYSTEM**

### **Default User Feedback Requirements**

**CRITICAL**: Every frontend application MUST implement a comprehensive notification system for user feedback, especially for API interactions and critical user actions.

#### **Required Notification Scenarios**

**API Interaction Notifications**:

- **API Call Failures**: Network errors, server errors (5xx), timeout errors
- **API Call Success**: Form submissions, data saves, record updates, deletions
- **Authentication Events**: Login/logout success, session expiration warnings
- **Validation Errors**: Client-side and server-side validation failures
- **Loading States**: Long-running operations, data fetching, file uploads

**System Event Notifications**:

- **Connection Status**: Network connectivity changes, offline mode
- **Data Sync**: Background synchronization status, conflict resolution
- **Feature Updates**: New features, maintenance notifications
- **Critical Alerts**: Security warnings, system maintenance

#### **Notification Types & Implementation**

**Using Ant Design Notification System**:

```javascript
import { notification, message } from "antd";

// Error Notifications (API Failures)
notification.error({
  message: "Operation Failed",
  description:
    "Unable to save changes. Please check your connection and try again.",
  duration: 6,
  placement: "topRight",
});

// Success Notifications
message.success("Changes saved successfully!");

// Loading States
message.loading("Saving changes...", 0);

// Warning Notifications
notification.warning({
  message: "Session Expiring",
  description: "Your session will expire in 5 minutes. Please save your work.",
  duration: 10,
});
```

**Notification Standards**:

- **Error (API Failures)**: Red theme, 6-8 second duration, actionable message
- **Success**: Green theme, 3-4 second duration, confirmation message
- **Warning**: Orange theme, 5-6 second duration, cautionary message
- **Info**: Blue theme, 4-5 second duration, informational message
- **Loading**: Auto-dismiss when operation completes

#### **Error Message Categories**

**Network & Server Errors**:

- **Network Error**: "Connection failed. Please check your internet connection and try again."
- **Server Error (5xx)**: "Something went wrong on our end. Please try again in a few moments."
- **Timeout Error**: "Request timed out. Please try again."
- **Rate Limit**: "Too many requests. Please wait a moment before trying again."

**Authentication & Authorization**:

- **Session Expired**: "Your session has expired. Please log in again to continue."
- **Unauthorized**: "You don't have permission to perform this action."
- **Invalid Credentials**: "Invalid username or password. Please try again."

**Validation & Data Errors**:

- **Validation Error**: "Please check the highlighted fields and correct any errors."
- **Duplicate Data**: "This record already exists. Please use a different value."
- **Missing Required Data**: "Please fill in all required fields before submitting."
- **Invalid Format**: "Please enter a valid [email/phone/date] format."

#### **Notification Positioning & Behavior**

**Desktop Layout**:

- **Primary Position**: Top-right corner for standard notifications
- **Critical Alerts**: Center modal overlay for important messages
- **Loading States**: Inline or center overlay depending on context

**Mobile Layout**:

- **Primary Position**: Top of screen, full width
- **Critical Alerts**: Full-screen overlay for important messages
- **Loading States**: Inline with touch-friendly dismiss options

**Accessibility Features**:

- **Screen Reader**: Proper ARIA labels and live regions
- **Keyboard Navigation**: Focus management and dismiss shortcuts
- **High Contrast**: Sufficient color contrast for all notification types
- **Reduced Motion**: Respect user motion preferences

#### **Implementation Pattern**

**HTTP Client with Automatic Notifications**:

```javascript
// API service with built-in error handling
class ApiService {
  constructor() {
    this.client = axios.create({
      baseURL: "/api",
      timeout: 10000,
    });

    this.setupInterceptors();
  }

  setupInterceptors() {
    // Request interceptor
    this.client.interceptors.request.use((config) => {
      if (config.showLoading !== false) {
        message.loading("Loading...", 0);
      }
      return config;
    });

    // Response interceptor
    this.client.interceptors.response.use(
      (response) => {
        message.destroy(); // Clear loading

        if (response.config.showSuccess) {
          message.success(
            response.config.successMessage ||
              "Operation completed successfully!"
          );
        }

        return response;
      },
      (error) => {
        message.destroy(); // Clear loading
        this.handleApiError(error);
        return Promise.reject(error);
      }
    );
  }

  handleApiError(error) {
    if (error.code === "NETWORK_ERROR") {
      notification.error({
        message: "Connection Error",
        description: "Please check your internet connection and try again.",
      });
    } else if (error.response?.status === 401) {
      notification.error({
        message: "Authentication Required",
        description: "Your session has expired. Please log in again.",
      });
    } else if (error.response?.status >= 500) {
      notification.error({
        message: "Server Error",
        description: "Something went wrong on our end. Please try again later.",
      });
    } else {
      notification.error({
        message: "Request Failed",
        description:
          error.response?.data?.message || "An unexpected error occurred.",
      });
    }
  }
}
```

**Form Submission with Notifications**:

```javascript
const handleSubmit = async (values) => {
  try {
    message.loading("Saving...", 0);

    await api.post("/submit", values, {
      showSuccess: true,
      successMessage: "Form submitted successfully!",
    });

    // Additional success actions
    form.resetFields();
    navigate("/success");
  } catch (error) {
    // Error automatically handled by interceptor
    console.error("Submission failed:", error);
  }
};
```

#### **Notification System Exceptions**

**When NOT to Use Default Notifications**:

- User explicitly requests silent mode or custom notification system
- Specialized applications where notifications interfere with workflow
- Real-time applications where notifications would be overwhelming
- Custom notification systems already implemented with equivalent functionality

## 🎨 **GAIA's UI/UX EXPERTISE** (When No Inspiration Provided)

### **Automatic Design Intelligence**

When users don't provide visual inspiration or UI/UX directives, GAIA automatically becomes the expert UI/UX designer, analyzing the target audience and crafting the perfect interface.

### **Audience-Driven Design Matrix**

#### **Business/Enterprise Applications**

**Characteristics**: Professional, trustworthy, efficient
**Color Palette**:

- Primary: Deep blues (#1E40AF, #3B82F6) or sophisticated grays (#374151, #6B7280)
- Accent: Professional greens (#059669, #10B981) or warm oranges (#EA580C, #F97316)
  **Typography**: Clean sans-serif (Inter, Roboto, Open Sans)
  **Layout**: Grid-based, data-dense, clear hierarchy
  **Examples**: Stripe, Linear, Notion, Salesforce Lightning

#### **Consumer/General Applications**

**Characteristics**: Friendly, approachable, intuitive
**Color Palette**:

- Primary: Warm blues (#2563EB, #3B82F6) or friendly purples (#7C3AED, #8B5CF6)
- Accent: Energetic colors (#EF4444, #F59E0B, #10B981)
  **Typography**: Rounded, friendly fonts (Inter, Poppins, Nunito)
  **Layout**: Card-based, whitespace-heavy, mobile-first
  **Examples**: Airbnb, Spotify, Instagram, Apple

#### **Creative/Portfolio Applications**

**Characteristics**: Bold, expressive, showcase-focused
**Color Palette**:

- Primary: Bold, artistic colors (#DC2626, #7C2D12, #1F2937)
- Accent: Vibrant, creative colors (#F59E0B, #8B5CF6, #EC4899)
  **Typography**: Distinctive fonts (Outfit, Playfair Display, custom)
  **Layout**: Asymmetrical, image-heavy, creative grids
  **Examples**: Behance, Dribbble, Awwwards, Adobe

#### **Technical/Developer Applications**

**Characteristics**: Functional, customizable, information-dense
**Color Palette**:

- Primary: Dark themes (#111827, #1F2937) with accent colors (#3B82F6, #10B981)
- Light: Clean grays (#F9FAFB, #F3F4F6) with technical blues
  **Typography**: Monospace options (JetBrains Mono, Fira Code) + sans-serif
  **Layout**: Dashboard-style, customizable panels, terminal-inspired
  **Examples**: GitHub, VS Code, Vercel, Figma

### **GAIA's Creative Process**

1. **Audience Analysis**: Extract target user type from project description
2. **Industry Research**: Apply industry-specific design patterns and expectations
3. **Color Psychology**: Select colors that evoke appropriate emotions and trust
4. **Information Architecture**: Design user flows that match user mental models
5. **Accessibility Integration**: Ensure inclusive design from the ground up
6. **Modern Trends Integration**: Apply current design trends appropriately

### **Default Design Decisions** (When Creating Original UI)

#### **Color Strategy**:

- **Primary Color**: Choose based on industry (blue for trust, green for growth, purple for creativity)
- **Accent Colors**: Complementary colors that enhance, not compete
- **Neutral Palette**: Modern grays with proper contrast ratios (4.5:1 minimum)
- **Semantic Colors**: Green for success, red for errors, amber for warnings, blue for info

#### **Typography Hierarchy**:

- **Display/Hero**: 3.5rem (56px) - Landing page headlines
- **H1**: 2.5rem (40px) - Page titles
- **H2**: 2rem (32px) - Section headers
- **H3**: 1.5rem (24px) - Subsection headers
- **Body Large**: 1.125rem (18px) - Important content
- **Body**: 1rem (16px) - Standard content
- **Small**: 0.875rem (14px) - Meta information
- **Caption**: 0.75rem (12px) - Fine print

#### **Spacing System** (8px base):

- **XS**: 4px - Icon spacing, small gaps
- **SM**: 8px - Element padding, tight spacing
- **MD**: 16px - Standard spacing between elements
- **LG**: 24px - Section spacing
- **XL**: 32px - Large section breaks
- **2XL**: 48px - Major layout divisions
- **3XL**: 64px - Hero section spacing

#### **Component Defaults**:

- **Buttons**: Rounded corners (8px), hover states, focus rings
- **Cards**: Subtle shadows, rounded corners (12px), proper padding
- **Forms**: Clear labels, proper spacing, validation states
- **Navigation**: Intuitive hierarchy, clear active states
- **Loading States**: Skeleton screens, progressive loading
- **Empty States**: Helpful illustrations, clear next steps

## 🎨 Visual Inspiration & Design Direction

### Design References

- **Primary Inspiration**: `[LINKS_TO_SPECIFIC_APPS/WEBSITES]`
- **Secondary References**: `[ADDITIONAL_INSPIRATION_SOURCES]`
- **Target Aesthetic**: `[MODERN_MINIMALIST/RICH_DETAILED/CREATIVE_BOLD/ENTERPRISE_PROFESSIONAL/ETC]`

### Design Philosophy

- **Core Principle**: `[BEAUTY_THROUGH_SIMPLICITY/SOPHISTICATED_DETAIL/BOLD_CREATIVITY/ETC]`
- **User Experience Goals**: `[INTUITIVE_NAVIGATION/DELIGHTFUL_INTERACTIONS/EFFICIENT_WORKFLOWS/ETC]`
- **Brand Personality**: `[TRUSTWORTHY/INNOVATIVE/PLAYFUL/PROFESSIONAL/ETC]`

## Design System

### Color Palette

**Primary Colors** (Based on inspiration/brand):

- Primary: `#[HEX_CODE]` - Main brand color for CTAs and primary actions
- Primary Light: `#[HEX_CODE]` - Hover states and backgrounds
- Primary Dark: `#[HEX_CODE]` - Active states and emphasis
- Secondary: `#[HEX_CODE]` - Accent color for highlights and secondary actions
- Tertiary: `#[HEX_CODE]` - Supporting color for variety and interest

**Neutral Palette** (Modern, sophisticated neutrals):

- White: `#FFFFFF` - Pure white for backgrounds
- Gray 50: `#[HEX_CODE]` - Lightest gray for subtle backgrounds
- Gray 100: `#[HEX_CODE]` - Very light gray for disabled states
- Gray 200: `#[HEX_CODE]` - Light gray for borders
- Gray 300: `#[HEX_CODE]` - Medium-light gray for secondary text
- Gray 400: `#[HEX_CODE]` - Medium gray for placeholders
- Gray 500: `#[HEX_CODE]` - True gray for secondary text
- Gray 600: `#[HEX_CODE]` - Dark gray for primary text
- Gray 700: `#[HEX_CODE]` - Very dark gray for headings
- Gray 800: `#[HEX_CODE]` - Almost black for emphasis
- Gray 900: `#[HEX_CODE]` - Pure black for maximum contrast

**Semantic Colors** (Modern, accessible):

- Success: `#10B981` - Green for success states
- Success Light: `#D1FAE5` - Light green for success backgrounds
- Warning: `#F59E0B` - Amber for warning states
- Warning Light: `#FEF3C7` - Light amber for warning backgrounds
- Error: `#EF4444` - Red for error states
- Error Light: `#FEE2E2` - Light red for error backgrounds
- Info: `#3B82F6` - Blue for informational states
- Info Light: `#DBEAFE` - Light blue for info backgrounds

## 🔔 **MANDATORY NOTIFICATION SYSTEM**

### **Default User Feedback Requirements**

**CRITICAL**: Every frontend application MUST implement a comprehensive notification system for user feedback, especially for API interactions and critical user actions.

#### **Required Notification Scenarios**

**API Interaction Notifications**:

- **API Call Failures**: Network errors, server errors (5xx), timeout errors
- **API Call Success**: Form submissions, data saves, record updates, deletions
- **Authentication Events**: Login/logout success, session expiration warnings
- **Validation Errors**: Client-side and server-side validation failures
- **Loading States**: Long-running operations, data fetching, file uploads

**System Event Notifications**:

- **Connection Status**: Network connectivity changes, offline mode
- **Data Sync**: Background synchronization status, conflict resolution
- **Feature Updates**: New features, maintenance notifications
- **Critical Alerts**: Security warnings, system maintenance

#### **Notification Types & Implementation**

**Using Ant Design Notification System**:

```javascript
import { notification, message } from "antd";

// Error Notifications (API Failures)
notification.error({
  message: "Operation Failed",
  description:
    "Unable to save changes. Please check your connection and try again.",
  duration: 6,
  placement: "topRight",
});

// Success Notifications
message.success("Changes saved successfully!");

// Loading States
message.loading("Saving changes...", 0);

// Warning Notifications
notification.warning({
  message: "Session Expiring",
  description: "Your session will expire in 5 minutes. Please save your work.",
  duration: 10,
});
```

**Notification Standards**:

- **Error (API Failures)**: Red theme, 6-8 second duration, actionable message
- **Success**: Green theme, 3-4 second duration, confirmation message
- **Warning**: Orange theme, 5-6 second duration, cautionary message
- **Info**: Blue theme, 4-5 second duration, informational message
- **Loading**: Auto-dismiss when operation completes

#### **Error Message Categories**

**Network & Server Errors**:

- **Network Error**: "Connection failed. Please check your internet connection and try again."
- **Server Error (5xx)**: "Something went wrong on our end. Please try again in a few moments."
- **Timeout Error**: "Request timed out. Please try again."
- **Rate Limit**: "Too many requests. Please wait a moment before trying again."

**Authentication & Authorization**:

- **Session Expired**: "Your session has expired. Please log in again to continue."
- **Unauthorized**: "You don't have permission to perform this action."
- **Invalid Credentials**: "Invalid username or password. Please try again."

**Validation & Data Errors**:

- **Validation Error**: "Please check the highlighted fields and correct any errors."
- **Duplicate Data**: "This record already exists. Please use a different value."
- **Missing Required Data**: "Please fill in all required fields before submitting."
- **Invalid Format**: "Please enter a valid [email/phone/date] format."

#### **Notification Positioning & Behavior**

**Desktop Layout**:

- **Primary Position**: Top-right corner for standard notifications
- **Critical Alerts**: Center modal overlay for important messages
- **Loading States**: Inline or center overlay depending on context

**Mobile Layout**:

- **Primary Position**: Top of screen, full width
- **Critical Alerts**: Full-screen overlay for important messages
- **Loading States**: Inline with touch-friendly dismiss options

**Accessibility Features**:

- **Screen Reader**: Proper ARIA labels and live regions
- **Keyboard Navigation**: Focus management and dismiss shortcuts
- **High Contrast**: Sufficient color contrast for all notification types
- **Reduced Motion**: Respect user motion preferences

#### **Implementation Pattern**

**HTTP Client with Automatic Notifications**:

```javascript
// API service with built-in error handling
class ApiService {
  constructor() {
    this.client = axios.create({
      baseURL: "/api",
      timeout: 10000,
    });

    this.setupInterceptors();
  }

  setupInterceptors() {
    // Request interceptor
    this.client.interceptors.request.use((config) => {
      if (config.showLoading !== false) {
        message.loading("Loading...", 0);
      }
      return config;
    });

    // Response interceptor
    this.client.interceptors.response.use(
      (response) => {
        message.destroy(); // Clear loading

        if (response.config.showSuccess) {
          message.success(
            response.config.successMessage ||
              "Operation completed successfully!"
          );
        }

        return response;
      },
      (error) => {
        message.destroy(); // Clear loading
        this.handleApiError(error);
        return Promise.reject(error);
      }
    );
  }

  handleApiError(error) {
    if (error.code === "NETWORK_ERROR") {
      notification.error({
        message: "Connection Error",
        description: "Please check your internet connection and try again.",
      });
    } else if (error.response?.status === 401) {
      notification.error({
        message: "Authentication Required",
        description: "Your session has expired. Please log in again.",
      });
    } else if (error.response?.status >= 500) {
      notification.error({
        message: "Server Error",
        description: "Something went wrong on our end. Please try again later.",
      });
    } else {
      notification.error({
        message: "Request Failed",
        description:
          error.response?.data?.message || "An unexpected error occurred.",
      });
    }
  }
}
```

**Form Submission with Notifications**:

```javascript
const handleSubmit = async (values) => {
  try {
    message.loading("Saving...", 0);

    await api.post("/submit", values, {
      showSuccess: true,
      successMessage: "Form submitted successfully!",
    });

    // Additional success actions
    form.resetFields();
    navigate("/success");
  } catch (error) {
    // Error automatically handled by interceptor
    console.error("Submission failed:", error);
  }
};
```

#### **Notification System Exceptions**

**When NOT to Use Default Notifications**:

- User explicitly requests silent mode or custom notification system
- Specialized applications where notifications interfere with workflow
- Real-time applications where notifications would be overwhelming
- Custom notification systems already implemented with equivalent functionality

## 🎨 **GAIA's UI/UX EXPERTISE** (When No Inspiration Provided)

### **Automatic Design Intelligence**

When users don't provide visual inspiration or UI/UX directives, GAIA automatically becomes the expert UI/UX designer, analyzing the target audience and crafting the perfect interface.

### **Audience-Driven Design Matrix**

#### **Business/Enterprise Applications**

**Characteristics**: Professional, trustworthy, efficient
**Color Palette**:

- Primary: Deep blues (#1E40AF, #3B82F6) or sophisticated grays (#374151, #6B7280)
- Accent: Professional greens (#059669, #10B981) or warm oranges (#EA580C, #F97316)
  **Typography**: Clean sans-serif (Inter, Roboto, Open Sans)
  **Layout**: Grid-based, data-dense, clear hierarchy
  **Examples**: Stripe, Linear, Notion, Salesforce Lightning

#### **Consumer/General Applications**

**Characteristics**: Friendly, approachable, intuitive
**Color Palette**:

- Primary: Warm blues (#2563EB, #3B82F6) or friendly purples (#7C3AED, #8B5CF6)
- Accent: Energetic colors (#EF4444, #F59E0B, #10B981)
  **Typography**: Rounded, friendly fonts (Inter, Poppins, Nunito)
  **Layout**: Card-based, whitespace-heavy, mobile-first
  **Examples**: Airbnb, Spotify, Instagram, Apple

#### **Creative/Portfolio Applications**

**Characteristics**: Bold, expressive, showcase-focused
**Color Palette**:

- Primary: Bold, artistic colors (#DC2626, #7C2D12, #1F2937)
- Accent: Vibrant, creative colors (#F59E0B, #8B5CF6, #EC4899)
  **Typography**: Distinctive fonts (Outfit, Playfair Display, custom)
  **Layout**: Asymmetrical, image-heavy, creative grids
  **Examples**: Behance, Dribbble, Awwwards, Adobe

#### **Technical/Developer Applications**

**Characteristics**: Functional, customizable, information-dense
**Color Palette**:

- Primary: Dark themes (#111827, #1F2937) with accent colors (#3B82F6, #10B981)
- Light: Clean grays (#F9FAFB, #F3F4F6) with technical blues
  **Typography**: Monospace options (JetBrains Mono, Fira Code) + sans-serif
  **Layout**: Dashboard-style, customizable panels, terminal-inspired
  **Examples**: GitHub, VS Code, Vercel, Figma

### **GAIA's Creative Process**

1. **Audience Analysis**: Extract target user type from project description
2. **Industry Research**: Apply industry-specific design patterns and expectations
3. **Color Psychology**: Select colors that evoke appropriate emotions and trust
4. **Information Architecture**: Design user flows that match user mental models
5. **Accessibility Integration**: Ensure inclusive design from the ground up
6. **Modern Trends Integration**: Apply current design trends appropriately

### **Default Design Decisions** (When Creating Original UI)

#### **Color Strategy**:

- **Primary Color**: Choose based on industry (blue for trust, green for growth, purple for creativity)
- **Accent Colors**: Complementary colors that enhance, not compete
- **Neutral Palette**: Modern grays with proper contrast ratios (4.5:1 minimum)
- **Semantic Colors**: Green for success, red for errors, amber for warnings, blue for info

#### **Typography Hierarchy**:

- **Display/Hero**: 3.5rem (56px) - Landing page headlines
- **H1**: 2.5rem (40px) - Page titles
- **H2**: 2rem (32px) - Section headers
- **H3**: 1.5rem (24px) - Subsection headers
- **Body Large**: 1.125rem (18px) - Important content
- **Body**: 1rem (16px) - Standard content
- **Small**: 0.875rem (14px) - Meta information
- **Caption**: 0.75rem (12px) - Fine print

#### **Spacing System** (8px base):

- **XS**: 4px - Icon spacing, small gaps
- **SM**: 8px - Element padding, tight spacing
- **MD**: 16px - Standard spacing between elements
- **LG**: 24px - Section spacing
- **XL**: 32px - Large section breaks
- **2XL**: 48px - Major layout divisions
- **3XL**: 64px - Hero section spacing

#### **Component Defaults**:

- **Buttons**: Rounded corners (8px), hover states, focus rings
- **Cards**: Subtle shadows, rounded corners (12px), proper padding
- **Forms**: Clear labels, proper spacing, validation states
- **Navigation**: Intuitive hierarchy, clear active states
- **Loading States**: Skeleton screens, progressive loading
- **Empty States**: Helpful illustrations, clear next steps

## 🎨 Visual Inspiration & Design Direction

### Design References

- **Primary Inspiration**: `[LINKS_TO_SPECIFIC_APPS/WEBSITES]`
- **Secondary References**: `[ADDITIONAL_INSPIRATION_SOURCES]`
- **Target Aesthetic**: `[MODERN_MINIMALIST/RICH_DETAILED/CREATIVE_BOLD/ENTERPRISE_PROFESSIONAL/ETC]`

### Design Philosophy

- **Core Principle**: `[BEAUTY_THROUGH_SIMPLICITY/SOPHISTICATED_DETAIL/BOLD_CREATIVITY/ETC]`
- **User Experience Goals**: `[INTUITIVE_NAVIGATION/DELIGHTFUL_INTERACTIONS/EFFICIENT_WORKFLOWS/ETC]`
- **Brand Personality**: `[TRUSTWORTHY/INNOVATIVE/PLAYFUL/PROFESSIONAL/ETC]`

## Design System

### Color Palette

**Primary Colors** (Based on inspiration/brand):

- Primary: `#[HEX_CODE]` - Main brand color for CTAs and primary actions
- Primary Light: `#[HEX_CODE]` - Hover states and backgrounds
- Primary Dark: `#[HEX_CODE]` - Active states and emphasis
- Secondary: `#[HEX_CODE]` - Accent color for highlights and secondary actions
- Tertiary: `#[HEX_CODE]` - Supporting color for variety and interest

**Neutral Palette** (Modern, sophisticated neutrals):

- White: `#FFFFFF` - Pure white for backgrounds
- Gray 50: `#[HEX_CODE]` - Lightest gray for subtle backgrounds
- Gray 100: `#[HEX_CODE]` - Very light gray for disabled states
- Gray 200: `#[HEX_CODE]` - Light gray for borders
- Gray 300: `#[HEX_CODE]` - Medium-light gray for secondary text
- Gray 400: `#[HEX_CODE]` - Medium gray for placeholders
- Gray 500: `#[HEX_CODE]` - True gray for secondary text
- Gray 600: `#[HEX_CODE]` - Dark gray for primary text
- Gray 700: `#[HEX_CODE]` - Very dark gray for headings
- Gray 800: `#[HEX_CODE]` - Almost black for emphasis
- Gray 900: `#[HEX_CODE]` - Pure black for maximum contrast

**Semantic Colors** (Modern, accessible):

- Success: `#10B981` - Green for success states
- Success Light: `#D1FAE5` - Light green for success backgrounds
- Warning: `#F59E0B` - Amber for warning states
- Warning Light: `#FEF3C7` - Light amber for warning backgrounds
- Error: `#EF4444` - Red for error states
- Error Light: `#FEE2E2` - Light red for error backgrounds
- Info: `#3B82F6` - Blue for informational states
- Info Light: `#DBEAFE` - Light blue for info backgrounds

## ✨ Modern Animations & Micro-interactions

### Timing & Easing (Smooth, Natural Feel)

**Transition Durations**:

- **Instant**: `0ms` (Immediate feedback)
- **Fast**: `150ms` (Quick hover states, small UI changes)
- **Medium**: `250ms` (Default for most interactions)
- **Slow**: `400ms` (Page transitions, complex animations)
- **Very Slow**: `600ms` (Special emphasis animations)

**Easing Functions** (Natural, physics-based):

- **Default**: `cubic-bezier(0.4, 0, 0.2, 1)` (Material Design standard)
- **Entrance**: `cubic-bezier(0, 0, 0.2, 1)` (Ease out - elements coming in)
- **Exit**: `cubic-bezier(0.4, 0, 1, 1)` (Ease in - elements going out)
- **Sharp**: `cubic-bezier(0.4, 0, 0.6, 1)` (Quick, snappy movements)
- **Bounce**: `cubic-bezier(0.68, -0.55, 0.265, 1.55)` (Playful bounce effect)

### Component Animations

**Button Interactions**:

- Hover: `transform: translateY(-1px)` + shadow increase over `150ms`
- Active: `transform: translateY(0px)` + shadow decrease over `100ms`
- Loading: Spinner or pulse animation
- Success: Brief scale animation `scale(1.05)` then back to `1.0`

**Card Animations**:

- Hover: `transform: translateY(-4px)` + shadow elevation over `250ms`
- Load-in: Fade in with `translateY(20px)` to `translateY(0)` over `400ms`
- Stagger: Cards animate in sequence with `100ms` delays

**Modal Animations**:

- Entrance:
  - Backdrop: Fade in over `250ms`
  - Modal: Scale from `0.95` to `1.0` + fade in over `300ms`
- Exit: Reverse of entrance over `200ms`

**Page Transitions**:

- Route changes: Fade + slight slide (`translateX(20px)`) over `400ms`
- Loading states: Skeleton screens with subtle shimmer animations

### Micro-interactions (Delightful Details)

**Interactive Feedback**:

- **Form Focus**: Smooth border color transition + subtle scale of focus ring
- **Checkbox/Radio**: Checkmark draw-in animation over `200ms`
- **Toggle Switches**: Smooth slide animation with bounce easing
- **Dropdown Expand**: Height expansion with opacity fade-in
- **Progress Indicators**: Smooth bar fill or circular progress
- **Success Actions**: Subtle confetti or checkmark animation

**Hover States**:

- **Links**: Underline animation from left to right
- **Images**: Subtle scale (`scale(1.05)`) with overflow hidden
- **Icons**: Color transition + optional rotation/bounce
- **Navigation Items**: Background slide-in animation

### Loading & State Animations

**Loading States**:

- **Skeleton Screens**: Shimmer animation across placeholder content
- **Spinners**: Smooth rotation with appropriate sizing
- **Progress Bars**: Smooth fill animation with optional pulse
- **Lazy Loading**: Fade-in as content loads

**Data Animations**:

- **Chart Transitions**: Smooth data updates with eased transitions
- **Number Counters**: Count-up animations for statistics
- **Sort/Filter**: Smooth reordering with translate animations

## 📱 Modern Responsive Design

### Mobile-First Strategy

**Mobile Layout Patterns** (320px+):

- Single column layouts
- Collapsible navigation (hamburger menu)
- Touch-friendly 44px+ button heights
- Swipe gestures for carousels/navigation
- Bottom-aligned primary actions

**Tablet Adaptations** (768px+):

- Two-column layouts where appropriate
- Expanded navigation (visible menu items)
- Side-by-side forms
- Larger touch targets maintained

**Desktop Enhancements** (1024px+):

- Multi-column layouts (up to 3-4 columns)
- Hover states and micro-interactions
- Larger imagery and more whitespace
- Advanced navigation patterns
- Keyboard shortcuts and accessibility

### Touch & Interaction Targets

**Minimum Sizes** (Accessibility compliant):

- Touch targets: `44px × 44px` minimum
- Spacing between targets: `8px` minimum
- Text links: `44px` height clickable area
- Form inputs: `44px` height minimum

## ♿ Accessibility & Inclusion

### Color & Contrast (WCAG AA+)

**Contrast Ratios**:

- Normal text: `4.5:1` minimum (WCAG AA)
- Large text (18px+): `3:1` minimum
- UI components: `3:1` minimum
- Focus indicators: `3:1` minimum

**Color Independence**:

- Never rely solely on color to convey information
- Use icons, text, or patterns as alternatives
- Support colorblind users with distinct patterns

### Keyboard & Screen Reader Support

**Focus Management**:

- Visible focus indicators with `2px` outline + `2px` offset
- Logical tab order following content flow
- Focus trapping in modals and dropdowns
- Skip links for main content areas

**ARIA & Semantic HTML**:

- Proper heading hierarchy (h1 → h2 → h3)
- ARIA labels for icon buttons and complex components
- Live regions for dynamic content updates
- Semantic landmarks (nav, main, aside, footer)

**Screen Reader Optimization**:

- Descriptive alt text for images
- Form labels explicitly associated with inputs
- Error messages linked to form fields
- Loading states announced to screen readers

## 🚀 Modern Technology Stack

### Core Framework & Build Tools

**Frontend Framework**:

- **React**: `18.x` with TypeScript for type safety and modern hooks
- **Next.js**: `14.x` for SSR/SSG, routing, and performance optimization (when applicable)
- **Vite**: `5.x` for lightning-fast development and optimized builds

**Package Management**:

- **pnpm**: Preferred for faster installs and efficient disk usage
- **npm**: Alternative if team preference or constraints require it

### Styling & Design Implementation

**CSS Strategy**:

- **Tailwind CSS**: `3.x` for utility-first styling with custom design system
- **CSS Modules**: For component-specific styles when needed
- **PostCSS**: For CSS processing and autoprefixing

**Component Libraries**:

- **Ant Design (Default)**: Primary component library with comprehensive React components, built-in theming, and professional design system
- **Alternative Options** (when specifically requested):
  - **Headless UI**: For accessible, unstyled components
  - **Radix UI**: For complex, accessible components
  - **Custom Components**: Built with design system specifications

### 🐜 **ANT DESIGN IMPLEMENTATION (DEFAULT)**

**CRITICAL**: Use Ant Design as the default component library for all frontends unless explicitly specified otherwise by the user.

#### **Core Ant Design Setup**:

- **Package**: `antd` latest stable version
- **Icons**: `@ant-design/icons` for comprehensive icon library
- **Styling**: `@ant-design/cssinjs` for CSS-in-JS theming
- **Date Handling**: Integrate with Day.js (Ant Design's preferred date library)

#### **Ant Design Component Usage**:

**Form Components** (Default choices):

- **Form**: `Form` component with built-in validation
- **Input**: `Input`, `Input.TextArea`, `Input.Password`
- **Select**: `Select` with search and multi-select capabilities
- **DatePicker**: `DatePicker`, `RangePicker` for date selections
- **Upload**: `Upload` with drag-and-drop support
- **Button**: `Button` with various types and sizes

**Layout Components**:

- **Layout**: `Layout`, `Header`, `Content`, `Footer`, `Sider`
- **Grid**: `Row` and `Col` for responsive layouts
- **Space**: `Space` for consistent spacing between elements
- **Divider**: `Divider` for visual separation

**Navigation Components**:

- **Menu**: `Menu` for navigation with nested items
- **Breadcrumb**: `Breadcrumb` for navigation hierarchy
- **Pagination**: `Pagination` for data navigation
- **Steps**: `Steps` for multi-step processes

**Data Display Components**:

- **Table**: `Table` with sorting, filtering, and pagination
- **List**: `List` for structured data display
- **Card**: `Card` for content containers
- **Descriptions**: `Descriptions` for detailed information display
- **Tag**: `Tag` for labels and categories

**Feedback Components**:

- **Alert**: `Alert` for important messages
- **Message**: `message` for global feedback
- **Notification**: `notification` for system notifications
- **Modal**: `Modal` for dialogs and confirmations
- **Popconfirm**: `Popconfirm` for action confirmations

#### **Ant Design Theming Configuration**:

**Custom Theme Setup**:

```typescript
import { ConfigProvider, theme } from "antd";

const customTheme = {
  token: {
    // Primary colors
    colorPrimary: "#1890ff", // Customize based on project
    colorSuccess: "#52c41a",
    colorWarning: "#faad14",
    colorError: "#f5222d",
    colorInfo: "#1890ff",

    // Layout
    borderRadius: 8,
    wireframe: false,

    // Typography
    fontSize: 14,
    fontFamily: "Inter, system-ui, sans-serif",
  },
  components: {
    Button: {
      borderRadius: 8,
      controlHeight: 44, // Accessibility-friendly height
    },
    Input: {
      borderRadius: 8,
      controlHeight: 44,
    },
    // ... other component customizations
  },
};
```

**Responsive Design with Ant Design**:

- Use Ant Design's built-in responsive grid system
- Leverage breakpoint utilities: `xs`, `sm`, `md`, `lg`, `xl`, `xxl`
- Implement responsive props for components (e.g., `Table` responsive scrolling)

#### **Integration with Design System**:

**Color Palette Integration**:

- Map project colors to Ant Design's token system
- Use `ConfigProvider` to apply custom color scheme
- Maintain semantic color meanings (success, warning, error)

**Typography Integration**:

- Configure Ant Design's typography tokens
- Use `Typography` component for consistent text styling
- Apply custom font families through theme configuration

**Spacing System Integration**:

- Utilize Ant Design's `Space` component for consistent spacing
- Configure custom spacing tokens if needed
- Maintain 8px grid system compatibility

#### **Ant Design Best Practices**:

**Performance Optimization**:

- Use tree-shaking to include only used components
- Implement proper `import` statements: `import { Button } from 'antd'`
- Configure babel-plugin-import for automatic tree-shaking

**Accessibility Compliance**:

- Leverage Ant Design's built-in accessibility features
- Test with keyboard navigation and screen readers
- Customize ARIA labels when needed

**Customization Guidelines**:

- Use CSS-in-JS theming rather than global CSS overrides
- Implement custom components that extend Ant Design components
- Maintain consistency with Ant Design's design language

#### **Tutorial System Integration**:

- **Tutorial Tooltips**: Use Ant Design's `Tooltip` and `Popover` components
- **Tour Component**: Utilize Ant Design's `Tour` component for guided tours
- **Progress Indicator**: Use `Progress` component for tutorial completion
- **Navigation**: Implement with `Button` components and consistent styling

#### **Common Component Patterns**:

**Form Implementation**:

```typescript
import { Form, Input, Button, Select, DatePicker } from "antd";

const MyForm = () => (
  <Form layout="vertical" onFinish={onFinish}>
    <Form.Item label="Name" name="name" rules={[{ required: true }]}>
      <Input placeholder="Enter your name" />
    </Form.Item>
    <Form.Item
      label="Email"
      name="email"
      rules={[{ required: true, type: "email" }]}
    >
      <Input placeholder="Enter your email" />
    </Form.Item>
    <Form.Item>
      <Button type="primary" htmlType="submit">
        Submit
      </Button>
    </Form.Item>
  </Form>
);
```

**Data Table Implementation**:

```typescript
import { Table, Space, Button } from "antd";

const columns = [
  {
    title: "Name",
    dataIndex: "name",
    key: "name",
  },
  {
    title: "Action",
    key: "action",
    render: (_, record) => (
      <Space size="middle">
        <Button type="link">Edit</Button>
        <Button type="link" danger>
          Delete
        </Button>
      </Space>
    ),
  },
];
```

#### **When NOT to Use Ant Design**:

- User explicitly requests a different component library
- Project requires highly custom, brand-specific components
- Performance requirements demand minimal bundle size
- Design system conflicts fundamentally with Ant Design's patterns

### State Management & Data Fetching

**State Management**:

- **Zustand**: Lightweight, modern state management for simple-medium projects
- **Redux Toolkit**: For complex state management needs
- **React Context**: For simple shared state

**Data Fetching**:

- **TanStack Query**: For server state management and caching
- **SWR**: Alternative for data fetching
- **Axios**: For HTTP client with interceptors

### Additional Libraries

**UI Enhancement**:

- **React Hook Form**: For performant, flexible forms
- **Framer Motion**: For beautiful animations and page transitions
- **React Hot Toast**: For elegant notification system
- **React Icons**: Comprehensive icon library
- **Date-fns**: For date manipulation and formatting

## 🎓 **MANDATORY TUTORIAL/ONBOARDING SYSTEM**

**CRITICAL**: Every frontend MUST include a comprehensive, built-in tutorial/onboarding system. This is a core requirement, not optional.

#### **Tutorial System Libraries**:

- **Primary**: Intro.js, Shepherd.js, or Reactour for React applications
- **Custom Implementation**: Overlay divs with z-index management for specific needs
- **State Management**: Tutorial progress tracking with localStorage persistence
- **Analytics**: Tutorial completion and drop-off tracking

#### **Tutorial System Components**:

**Core Tutorial Components**:

- **Tutorial Overlay**: Semi-transparent backdrop (rgba(0,0,0,0.7)) with spotlight effect
- **Tutorial Tooltip**: Positioned tooltip with arrow, description, and navigation controls
- **Progress Indicator**: Visual progress bar showing tutorial completion (e.g., "3 of 8")
- **Navigation Controls**: Previous, Next, Skip, and Exit buttons
- **Tutorial Menu**: Always-accessible help menu for re-starting tutorials

**Tutorial Content Structure**:

1. **Welcome Screen**: Brief app introduction with key value propositions
2. **Navigation Tour**: How to move around the application (menu, breadcrumbs, etc.)
3. **Core Features**: 3-5 most important features with interactive demonstrations
4. **Primary Actions**: Key actions users will perform regularly
5. **Help & Support**: Where to find documentation, contact support, or get help

#### **Implementation Specifications**:

**Visual Design**:

- **Spotlight Effect**: Highlighted element with 8px border-radius, white border
- **Backdrop**: Semi-transparent overlay (rgba(0,0,0,0.7)) covering entire viewport
- **Tooltip Design**: White background, Level 4 shadow, 12px border-radius
- **Typography**: Body M for descriptions, Label for buttons
- **Colors**: Primary color for action buttons, Gray-600 for secondary text
- **Animation**: 300ms smooth transitions between steps

**Responsive Behavior**:

- **Mobile**: Tooltip positioning adapts to avoid viewport edges
- **Tablet**: Larger tooltip sizes with more comfortable spacing
- **Desktop**: Full-featured tooltips with detailed descriptions

**Accessibility**:

- **Keyboard Navigation**: Arrow keys, Enter, and Esc key support
- **Screen Reader**: ARIA labels and announcements for tutorial steps
- **Focus Management**: Proper focus trapping and restoration
- **Skip Options**: Easy skip/exit options for experienced users

#### **Audience-Specific Tutorial Adaptations**:

**Business/Enterprise Applications**:

- Focus on efficiency, workflow optimization, and data insights
- Highlight reporting features, collaboration tools, and integrations
- Emphasize security features and admin controls

**Consumer/General Applications**:

- Emphasize fun, discovery, and social features
- Show personalization options and customization
- Highlight sharing and social interaction features

**Creative/Portfolio Applications**:

- Showcase creation tools and artistic features
- Highlight customization options and themes
- Show portfolio organization and presentation features

**Technical/Developer Applications**:

- Show advanced features, integrations, and API access
- Highlight customization options and developer tools
- Demonstrate automation features and workflow optimization

#### **Quality Requirements**:

- Track completion rates and identify drop-off points
- Update tutorials when UI changes
- Test tutorials on all supported devices and browsers
- Automated tests for tutorial functionality

## 📁 Modern File Structure

```
src/
├── app/                    # Next.js app directory (if using App Router)
│   ├── globals.css        # Global styles and Tailwind imports
│   ├── layout.tsx         # Root layout component
│   └── page.tsx           # Home page
├── components/
│   ├── ui/                # Base design system components
│   │   ├── Button.tsx     # Button variants
│   │   ├── Input.tsx      # Form inputs
│   │   ├── Card.tsx       # Card component
│   │   ├── Modal.tsx      # Modal/dialog system
│   │   └── index.ts       # Component exports
│   ├── forms/             # Form-specific components
│   │   ├── LoginForm.tsx
│   │   ├── ContactForm.tsx
│   │   └── index.ts
│   ├── layout/            # Layout components
│   │   ├── Header.tsx     # Main navigation
│   │   ├── Sidebar.tsx    # Side navigation
│   │   ├── Footer.tsx     # Footer component
│   │   └── index.ts
│   └── features/          # Feature-specific components
│       ├── dashboard/
│       ├── profile/
│       └── settings/
├── hooks/                 # Custom React hooks
│   ├── useAuth.ts        # Authentication logic
│   ├── useLocalStorage.ts
│   └── useDebounce.ts
├── lib/                   # Utility libraries and configurations
│   ├── auth.ts           # Authentication utilities
│   ├── api.ts            # API client setup
│   ├── utils.ts          # General utilities
│   └── validations.ts    # Form validation schemas
├── stores/               # State management
│   ├── authStore.ts     # Authentication state
│   ├── uiStore.ts       # UI state (modals, loading, etc.)
│   └── index.ts
├── styles/               # Styling files
│   ├── globals.css      # Global styles
│   ├── components.css   # Component-specific styles
│   └── tailwind.css     # Tailwind configuration
├── types/                # TypeScript type definitions
│   ├── auth.ts          # Authentication types
│   ├── api.ts           # API response types
│   └── global.ts        # Global type definitions
└── constants/            # Application constants
    ├── routes.ts        # Route definitions
    ├── api.ts           # API endpoints
    └── ui.ts            # UI constants (colors, sizes, etc.)
```

## 🎯 Implementation Best Practices

### Performance Optimization

**Bundle Optimization**:

- Code splitting at route and component levels
- Dynamic imports for heavy components
- Tree shaking for unused code elimination
- Asset optimization (images, fonts, CSS)

**Runtime Performance**:

- React.memo for expensive components
- useMemo and useCallback for expensive calculations
- Virtual scrolling for large data sets
- Image optimization with Next.js Image component

**Loading Strategies**:

- Skeleton screens for better perceived performance
- Progressive loading for images and content
- Lazy loading for below-the-fold content
- Service workers for caching (when appropriate)

### Developer Experience

**Type Safety**:

- Strict TypeScript configuration
- API response typing with Zod or similar
- Component prop interfaces
- Custom hook typing

**Code Quality**:

- ESLint with React and TypeScript rules
- Prettier for consistent formatting
- Husky for pre-commit hooks
- Conventional commits for better git history

### Testing Strategy

**Unit Testing**:

- **Vitest**: Fast unit testing framework
- **React Testing Library**: Component testing
- **MSW**: API mocking for tests

**Integration Testing**:

- **Playwright**: End-to-end testing
- **Storybook**: Component development and visual testing

## 🎨 Design System Implementation

### Tailwind Configuration

```javascript
// tailwind.config.js - Custom design system
module.exports = {
  content: ["./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        primary: {
          50: "#[PRIMARY_LIGHT]",
          500: "#[PRIMARY_BASE]",
          900: "#[PRIMARY_DARK]",
        },
        gray: {
          50: "#F9FAFB",
          100: "#F3F4F6",
          // ... rest of gray scale
        },
      },
      fontFamily: {
        sans: ["Inter", "system-ui", "sans-serif"],
        display: ["Outfit", "system-ui", "sans-serif"],
      },
      spacing: {
        18: "4.5rem",
        88: "22rem",
      },
      boxShadow: {
        "level-1": "0 1px 2px 0 rgba(0, 0, 0, 0.05)",
        "level-2":
          "0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06)",
        // ... rest of shadow levels
      },
    },
  },
  plugins: [require("@tailwindcss/forms"), require("@tailwindcss/typography")],
};
```

### Component Implementation Example

```typescript
// components/ui/Button.tsx - Type-safe, accessible button
interface ButtonProps extends React.ButtonHTMLAttributes<HTMLButtonElement> {
  variant?: "primary" | "secondary" | "ghost";
  size?: "sm" | "md" | "lg";
  loading?: boolean;
  children: React.ReactNode;
}

export const Button: React.FC<ButtonProps> = ({
  variant = "primary",
  size = "md",
  loading = false,
  children,
  className,
  disabled,
  ...props
}) => {
  const baseClasses =
    "inline-flex items-center justify-center font-medium rounded-lg transition-all duration-150 focus:outline-none focus:ring-2 focus:ring-offset-2";

  const variantClasses = {
    primary:
      "bg-primary-500 text-white hover:bg-primary-600 focus:ring-primary-500",
    secondary:
      "bg-white text-primary-500 border border-primary-500 hover:bg-primary-50 focus:ring-primary-500",
    ghost:
      "bg-transparent text-gray-600 hover:bg-gray-100 hover:text-gray-800 focus:ring-gray-500",
  };

  const sizeClasses = {
    sm: "px-3 py-2 text-sm",
    md: "px-6 py-3 text-base",
    lg: "px-8 py-4 text-lg",
  };

  return (
    <button
      className={cn(
        baseClasses,
        variantClasses[variant],
        sizeClasses[size],
        (disabled || loading) && "opacity-50 cursor-not-allowed",
        className
      )}
      disabled={disabled || loading}
      {...props}
    >
      {loading && <Spinner className="mr-2" />}
      {children}
    </button>
  );
};
```

## 📊 Success Metrics & Quality Gates

### Performance Targets

- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Cumulative Layout Shift**: < 0.1
- **First Input Delay**: < 100ms
- **Lighthouse Score**: 90+ for all categories

### Accessibility Goals

- **WCAG AA Compliance**: 100% for all interactive elements
- **Keyboard Navigation**: Full functionality without mouse
- **Screen Reader Support**: Comprehensive ARIA implementation
- **Color Contrast**: Minimum 4.5:1 for all text

## 🎨 CRITICAL: Visual Quality Assurance & Testing Protocol

### ⚠️ MANDATORY Visual Testing Requirements

**NEVER ASSUME BEAUTY** - Don't assume the frontend is beautifully implemented. ALWAYS rely on Playwright screenshot tests to ensure visual quality and design conformity.

### Visual Testing Implementation Strategy

#### 1. Screenshot Test Coverage

**Required Screenshot Tests**:

- **Homepage/Landing**: Desktop (1920x1080), Tablet (768x1024), Mobile (375x667)
- **All Major Pages**: Dashboard, Profile, Settings, etc. at all breakpoints
- **Component States**: Hover, focus, loading, error, empty states
- **Form Interactions**: Focus states, validation errors, success states
- **Navigation**: Open/closed states, responsive menu behavior
- **Modals & Overlays**: Proper positioning and backdrop rendering

#### 2. Visual Quality Checklist

**Contrast & Color Analysis**:

- [ ] All text meets WCAG AA contrast ratios (4.5:1 minimum)
- [ ] No jarring color combinations (e.g., black text on purple backgrounds)
- [ ] Consistent color palette application across all components
- [ ] Proper semantic color usage (success=green, error=red, etc.)
- [ ] Brand colors applied consistently

**Typography & Spacing**:

- [ ] Consistent font sizes and weights throughout
- [ ] Proper line heights for readability
- [ ] Consistent spacing between elements
- [ ] Proper heading hierarchy (h1→h2→h3)
- [ ] Text doesn't break or overflow containers

**Layout & Responsive Design**:

- [ ] No horizontal scrolling on mobile devices
- [ ] Touch targets are minimum 44px on mobile
- [ ] Elements stack properly at different screen sizes
- [ ] No overlapping or cut-off content
- [ ] Consistent alignment and grid structure

**Interactive Elements**:

- [ ] Clear hover states for all interactive elements
- [ ] Focus indicators visible and well-designed
- [ ] Loading states are visually appealing
- [ ] Error states are clear but not aggressive
- [ ] Success states provide positive feedback

#### 3. Playwright Visual Testing Implementation

**Test Structure Example**:

```javascript
// tests/visual/homepage.spec.ts
import { test, expect } from "@playwright/test";

test.describe("Homepage Visual Tests", () => {
  test("Homepage displays correctly across all breakpoints", async ({
    page,
  }) => {
    await page.goto("/");

    // Wait for page to fully load
    await page.waitForLoadState("networkidle");

    // Desktop screenshot
    await page.setViewportSize({ width: 1920, height: 1080 });
    await expect(page).toHaveScreenshot("homepage-desktop.png", {
      fullPage: true,
      animations: "disabled",
    });

    // Tablet screenshot
    await page.setViewportSize({ width: 768, height: 1024 });
    await expect(page).toHaveScreenshot("homepage-tablet.png", {
      fullPage: true,
      animations: "disabled",
    });

    // Mobile screenshot
    await page.setViewportSize({ width: 375, height: 667 });
    await expect(page).toHaveScreenshot("homepage-mobile.png", {
      fullPage: true,
      animations: "disabled",
    });
  });

  test("Interactive states render correctly", async ({ page }) => {
    await page.goto("/");

    // Test button hover states
    const primaryButton = page.locator('[data-testid="primary-cta"]');
    await primaryButton.hover();
    await expect(page).toHaveScreenshot("button-hover-state.png");

    // Test form focus states
    const emailInput = page.locator('input[type="email"]');
    await emailInput.focus();
    await expect(page).toHaveScreenshot("form-focus-state.png");

    // Test navigation menu
    await page.locator('[data-testid="menu-toggle"]').click();
    await expect(page).toHaveScreenshot("navigation-open.png");
  });

  test("Error and loading states display properly", async ({ page }) => {
    // Mock API error
    await page.route("**/api/**", (route) =>
      route.fulfill({ status: 500, body: "Server Error" })
    );

    await page.goto("/dashboard");
    await expect(page).toHaveScreenshot("error-state.png");

    // Test loading state
    await page.route(
      "**/api/**",
      (route) =>
        new Promise((resolve) =>
          setTimeout(() => resolve(route.continue()), 2000)
        )
    );

    await page.reload();
    await expect(page).toHaveScreenshot("loading-state.png");
  });
});
```

#### 4. Visual Quality Police Protocol

**Review Process**:

1. **Take Screenshots**: Capture all major pages and components
2. **Analyze Contrast**: Use browser dev tools to check color contrast ratios
3. **Compare to Design**: Reference the visual inspiration and design specs
4. **Identify Issues**: Document any visual problems or inconsistencies
5. **Fix and Re-test**: Implement fixes and re-run visual tests
6. **Iterate Until Perfect**: Continue until all visual tests pass

**Common Issues to Watch For**:

- Text that's too light on backgrounds (poor contrast)
- Elements that are cut off or overflow
- Inconsistent spacing or alignment
- Buttons or links that don't look clickable
- Missing hover or focus states
- Broken responsive layouts
- Colors that clash or look unprofessional
- Typography that's too small or hard to read
- Loading states that look broken or confusing

#### 5. Automated Visual Regression Testing

**CI/CD Integration**:

```yaml
# .github/workflows/visual-tests.yml
name: Visual Regression Tests
on: [push, pull_request]

jobs:
  visual-tests:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: "18"

      - name: Install dependencies
        run: npm ci

      - name: Install Playwright
        run: npx playwright install --with-deps

      - name: Run visual tests
        run: npx playwright test --grep "Visual Tests"

      - uses: actions/upload-artifact@v3
        if: failure()
        with:
          name: visual-regression-results
          path: |
            tests/visual/screenshots/**/*.png
            tests/visual/videos/**/*.webm
```
