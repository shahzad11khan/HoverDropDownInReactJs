# HoverDropDownInReactJs

  const [isOpenManagement, setIsOpenManagement] = useState(false);
  const [isOpen, setIsOpen] = useState(false);


  <div>
              <li
                className="flex items-center p-4 cursor-pointer hover:bg-gray-100 rounded-lg"
                onMouseEnter={() => setIsOpenManagement(true)}
                onMouseLeave={() => setIsOpenManagement(false)}
              >
                <div className="flex items-center gap-3 relative">
                  <FaCar className="text-custom-blue text-xl" />
                  <MdManageSearch className="text-custom-blue text-xl" />
                  <span className="hidden sm:block">Vehicle Management</span>

                  {/* Dropdown Menu */}
                  {isOpenManagement && (
                    <div className="absolute left-2 ml-60 mt-2 w-[400px] bg-white border border-gray-300 rounded-md shadow-lg z-10">
                      <ul className="grid grid-cols-2 space-y-1 p-2">
                        <li>
                          <Link
                            href="/Dashboard/Models/Manufacturer/GetManufacturers"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Manufacturers
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/VehicleType/GetVehicleTypes"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Vehicle Types
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Enquiry/GetEnquiries"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Enquiries
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Firm/GetFirms"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Firms
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Signature/GetSignatures"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Signatures
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/LocalAuthority/GetLocalAuthority"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Local Authority
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Supplier/GetSuppliers"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Suppliers
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Employee/GetEmployees"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Employees
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Badge/GetBadges"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Badges
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Insurance/GetInsurances"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Insurances
                          </Link>
                        </li>
                        <li>
                          <Link
                            href="/Dashboard/Models/Payment/GetPayments"
                            className="px-4 py-2 rounded hover:bg-gray-200"
                          >
                            All Payments
                          </Link>
                        </li>
                      </ul>
                    </div>
                  )}
                </div>
              </li>
            </div>

            {/*  */}
            <div className="">
              <li
                className="flex items-center p-4 cursor-pointer hover:bg-gray-100 rounded-lg"
                onMouseEnter={() => setIsOpen(true)}
                onMouseLeave={() => setIsOpen(false)}
              >
                <TbReport className="text-custom-blue text-xl" />
                <div className="relative inline-block">
                  <span className="items-center cursor-pointer hover:bg-gray-100 rounded-lg hidden sm:block ml-2">
                    Reports
                  </span>
                  {isOpen && (
                    <div className="absolute left-2 mt-2 w-auto bg-white border border-gray-300 rounded-md shadow-lg">
                      <ul className="flex flex-row space-x-4">
                        {/* System Reports Dropdown */}
                        <li
                          className="relative hover:bg-gray-100 cursor-pointer"
                          onMouseEnter={() => handleMouseEnter("systemReports")}
                          onMouseLeave={handleMouseLeave}
                        >
                          <Link
                            href="#"
                            className="block px-4 py-2 text-gray-800"
                          >
                            System Reports
                          </Link>
                          {openDropdown === "systemReports" && (
                            <ul className="absolute left-0 mt-2 w-[300px] bg-white border border-gray-300 rounded-md shadow-lg space-y-2 p-4">
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Employee Update Reports
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Rental Invoice Reports
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Overdue Payment Reports
                                </Link>
                              </li>
                            </ul>
                          )}
                        </li>

                        {/* Vehicle Reports Dropdown */}
                        <li
                          className="relative hover:bg-gray-100 cursor-pointer"
                          onMouseEnter={() =>
                            handleMouseEnter("vehicleReports")
                          }
                          onMouseLeave={handleMouseLeave}
                        >
                          <Link
                            href="#"
                            className="block px-4 py-2 text-gray-800"
                          >
                            Vehicle Reports
                          </Link>
                          {openDropdown === "vehicleReports" && (
                            <ul className="absolute left-0 mt-2 w-[300px] bg-white border border-gray-300 rounded-md shadow-lg space-y-2 p-4">
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Interim Test Expiry
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Mot Expiry
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Road Tax Expiry
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Test Date Expiry
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Plate Expiry
                                </Link>
                              </li>
                            </ul>
                          )}
                        </li>

                        {/* Driver Reports Dropdown */}
                        <li
                          className="relative hover:bg-gray-100 cursor-pointer"
                          onMouseEnter={() => handleMouseEnter("driverReports")}
                          onMouseLeave={handleMouseLeave}
                        >
                          <Link
                            href="#"
                            className="block px-4 py-2 text-gray-800"
                          >
                            Driver Reports
                          </Link>
                          {openDropdown === "driverReports" && (
                            <ul className="absolute left-0 mt-2 w-60 bg-white border border-gray-300 rounded-md shadow-lg space-y-2 p-4">
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-1 rounded hover:bg-gray-200"
                                >
                                  Drivers Holidays
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Licence Expiry
                                </Link>
                              </li>
                              <li>
                                <Link
                                  href="#"
                                  className="px-4 py-2 rounded hover:bg-gray-200"
                                >
                                  Taxi Badge Expiry
                                </Link>
                              </li>
                            </ul>
                          )}
                        </li>
                      </ul>
                    </div>
                  )}
                </div>
              </li>
            </div>
            {/*  */}
