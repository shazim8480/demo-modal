```typescript

import { Dialog, Transition } from "@headlessui/react";
import { Fragment } from "react";

export default function Modal({
  modalVisible,
  setModalVisible,
  title,
  bodyText,
  onBtnClick,
}: any) {
  return (
    <>
      <Transition appear show={modalVisible} as={Fragment}>
        <Dialog
          as="div"
          className="relative z-10"
          onClose={() => setModalVisible(false)}
        >
          <Transition.Child
            as={Fragment}
            enter="ease-out duration-300"
            enterFrom="opacity-0"
            enterTo="opacity-100"
            leave="ease-in duration-200"
            leaveFrom="opacity-100"
            leaveTo="opacity-0"
          >
            <div className="fixed inset-0 bg-black bg-opacity-25" />
          </Transition.Child>

          <div className="fixed inset-0 overflow-y-auto">
            <div className="flex items-center justify-center min-h-full p-4 text-center">
              <Transition.Child
                as={Fragment}
                enter="ease-out duration-300"
                enterFrom="opacity-0 scale-95"
                enterTo="opacity-100 scale-100"
                leave="ease-in duration-200"
                leaveFrom="opacity-100 scale-100"
                leaveTo="opacity-0 scale-95"
              >
                <Dialog.Panel className="w-full max-w-md p-6 overflow-hidden text-left align-middle transition-all transform bg-white shadow-xl rounded-2xl">
                  <Dialog.Title
                    as="h3"
                    className="text-lg font-medium leading-6 text-gray-900"
                  >
                    {title}
                  </Dialog.Title>
                  <div className="my-6">
                    <p className="text-sm text-gray-500">{bodyText}</p>
                  </div>

                  <div className="mt-4">
                    <button
                      type="button"
                      className="inline-flex justify-end px-4 py-2 text-sm font-medium bg-green-700 border border-transparent rounded-md text-green-50 hover:bg-green-800 "
                      onClick={onBtnClick}
                    >
                      Confirm
                    </button>
                    <button
                      type="button"
                      className="inline-flex justify-end px-4 py-2 ml-3 text-sm font-medium bg-red-700 border border-transparent rounded-md text-red-50 hover:bg-red-800 "
                      onClick={() => setModalVisible(false)}
                    >
                      Cancel
                    </button>
                  </div>
                </Dialog.Panel>
              </Transition.Child>
            </div>
          </div>
        </Dialog>
      </Transition>
    </>
  );
}

```
## Significance of the modal:

**1. Reusable and Adaptable:**    

This component is built to be incredibly versatile and adaptable. Its modular design allows for easy customization and seamless integration into different parts of your application. This saves you time and effort in the development process and ensures a consistent user experience across your project.  

**2. Simplified Development with Headless UI:**    

Leveraging the popular @headlessui/react library, this modal simplifies the development process while ensuring accessibility compliance. This powerful library provides a robust foundation for further customization, allowing you to tailor the modal to your specific needs.  

**3. Enhanced User Experience with Animations and Transitions:**    

Smooth animations and transitions for the modal's appearance and disappearance ensure a delightful and engaging user experience. These enhancements add a touch of professionalism and polish to your application, making interactions with the modal feel intuitive and natural.  

**4. Easy Customization with Clear Props:**    

The component utilizes clear and well-defined props that are easy to understand and use. Simply adjust the values of these props to customize the behavior and appearance of the modal to meet your specific requirements. This reduces the learning curve and allows for quick and efficient integration into your application.  

## Focus on Best Practices:

This modal component is built with best practices in mind, ensuring its maintainability, reliability, and accessibility:

**1. Modular Design:** Simplifies future modifications and maintenance.  
**2. Accessibility:** Prioritizes appropriate semantic elements and adherence to accessibility guidelines.  
**3. Code Clarity and Documentation:** Clear code structure and comments facilitate understanding and collaboration.  

